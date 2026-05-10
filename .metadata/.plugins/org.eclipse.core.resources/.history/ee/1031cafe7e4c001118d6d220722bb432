/*
 * main.c
 *
 *  Created on: 2026. 5. 10.
 *      Author: justjhst
 */

#include "stm32f446xx.h"
#include "stm32f446xx_gpio_driver.h"

int main(void)
{
	GPIO_Handle_t GpioLed, GpioBtn;

	GpioLed.pGPIOx = GPIOA;
	GpioLed.GPIO_PinConfig.GPIO_PinNumber = GPIO_PIN_NO_6;
	GpioLed.GPIO_PinConfig.GPIO_PinMode = GPIO_MODE_OUTPUT;
	GpioLed.GPIO_PinConfig.GPIO_Pin_Speed = GPIO_SPEED_LOW;
	GpioLed.GPIO_PinConfig.GPIO_PinOPtype = GPIO_OPTYPE_PP;
	GpioLed.GPIO_PinConfig.GPIO_PinPuPdControl = GPIO_NO_PUPD;

	GPIO_PeriClockControl(GPIOA, ENABLE);

	GPIO_Init(&GpioLed);

	GpioBtn.pGPIOx = GPIOB;
	GpioBtn.GPIO_PinConfig.GPIO_PinNumber = GPIO_PIN_NO_12;
	GpioBtn.GPIO_PinConfig.GPIO_PinMode = GPIO_MODE_IT_FT;
	GpioBtn.GPIO_PinConfig.GPIO_Pin_Speed = GPIO_SPEED_FAST;
	GpioBtn.GPIO_PinConfig.GPIO_PinPuPdControl = GPIO_PU;

	GPIO_PeriClockControl(GPIOB, ENABLE);
	GPIO_Init(&GpioBtn);

	GPIO_IRQPriorityConfig(40, 15);
	GPIO_IRQITConfig(40, ENABLE);


	while(1);
}

void EXTI15_10_IRQHandler(void)
{
	GPIO_IRQHandling(GPIO_PIN_NO_12);
	GPIO_ToggleOutputPin(GPIOA, GPIO_PIN_NO_6);
}



