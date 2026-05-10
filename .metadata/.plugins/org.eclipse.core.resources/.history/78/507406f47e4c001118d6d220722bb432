/*
 * stm32f446xx.h
 *
 *  Created on: 2026. 4. 27.
 *      Author: justjhst
 */

#ifndef INC_STM32F446XX_H_
#define INC_STM32F446XX_H_

#include <stdint.h>

#define __vo volatile

#define NVIC_ISER0									((__vo uint32_t*)0xE000E100)
#define NVIC_ISER1									((__vo uint32_t*)0xE000E104)
#define NVIC_ISER2									((__vo uint32_t*)0xE000E108)
#define NVIC_ISER3									((__vo uint32_t*)0xE000E10C)

#define NVIC_ICER0									((__vo uint32_t*)0xE000E180)
#define NVIC_ICER1									((__vo uint32_t*)0xE000E184)
#define NVIC_ICER2									((__vo uint32_t*)0xE000E188)
#define NVIC_ICER3									((__vo uint32_t*)0xE000E18C)

#define NVIC_PR_BASEADDR 							((__vo uint32_t*)0xE000E400)

#define NO_PR_BITS_IMPLEMENTED						4

#define FLASH_BASEADDR								0x08000000U

#define SRAM1_BASEADDR								0x20000000U
#define SRAM2_BASEADDR								0x2001C000U
#define ROM											0x1FFF0000U
#define SRAM 											SRAM1_BASEADDR

// RCC

#define PERIPH_BASE									0x40000000U
#define APB1PERIPH_BASE								PERIPH_BASE
#define APB2PERIPH_BASE								0x40010000U
#define AHB1PERIPH_BASE								0x40020000U
#define AHB2PERIPH_BASE								0x50000000U
#define AHB3PERIPH_BASE								0x60000000U

// AHB1

#define GPIOA_BASEADDR								(AHB1PERIPH_BASE + 0x0000)
#define GPIOB_BASEADDR								(AHB1PERIPH_BASE + 0x0400)
#define GPIOC_BASEADDR								(AHB1PERIPH_BASE + 0x0800)
#define GPIOD_BASEADDR								(AHB1PERIPH_BASE + 0x0C00)
#define GPIOE_BASEADDR								(AHB1PERIPH_BASE + 0x1000)
#define GPIOF_BASEADDR								(AHB1PERIPH_BASE + 0x1400)
#define GPIOG_BASEADDR								(AHB1PERIPH_BASE + 0x1800)
#define GPIOH_BASEADDR								(AHB1PERIPH_BASE + 0x1C00)
#define RCC_BASEADDR									(AHB1PERIPH_BASE + 0X3800)
// APB1

#define SPI2_I2S2_BASEADDR							(APB1PERIPH_BASE + 0x3800)
#define SPI3_I2S3_BASEADDR							(APB1PERIPH_BASE + 0x3C00)
#define USART2_BASEADDR								(APB1PERIPH_BASE + 0x4400)
#define USART3_BASEADDR								(APB1PERIPH_BASE + 0x4800)
#define UART4_BASEADDR								(APB1PERIPH_BASE + 0x4C00)
#define UART5_BASEADDR								(APB1PERIPH_BASE + 0x5000)
#define I2C1_BASEADDR								(APB1PERIPH_BASE + 0x5400)
#define I2C2_BASEADDR								(APB1PERIPH_BASE + 0x5800)
#define I2C3_BASEADDR								(APB1PERIPH_BASE + 0x5C00)
#define CAN1_BASEADDR								(APB1PERIPH_BASE + 0x6400)
#define CAN2_BASEADDR								(APB1PERIPH_BASE + 0x6800)

// APB2

#define USART1_BASEADDR								(APB2PERIPH_BASE + 0x1000)
#define USART6_BASEADDR								(APB2PERIPH_BASE + 0x1400)
#define SPI1_BASEADDR								(APB2PERIPH_BASE + 0x3000)
#define SPI4_BASEADDR								(APB2PERIPH_BASE + 0x3400)
#define SYSCFG_BASEADDR								(APB2PERIPH_BASE + 0x3800)
#define EXTI_BASEADDR								(APB2PERIPH_BASE + 0x3C00)


// peripheral register definition structures

typedef struct
{
	__vo uint32_t MODER;
	__vo uint32_t OTYPER;
	__vo uint32_t OSPEEDR;
	__vo uint32_t PUPDR;
	__vo uint32_t IDR;
	__vo uint32_t ODR;
	__vo uint32_t BSRR;
	__vo uint32_t LCKR;
	__vo uint32_t AFR[2];
	// AFR[0] : GPIO alternate function Low register, AFR[1] : GPIO alternate function high register
}GPIO_RegDef_t;

typedef struct {
	volatile uint32_t CR;
	volatile uint32_t PLLCFGR;
	volatile uint32_t CFGR;
	volatile uint32_t CIR;
	volatile uint32_t AHB1RSTR;
	volatile uint32_t AHB2RSTR;
	volatile uint32_t AHB3RSTR;
	volatile uint32_t RESERVED0;
	volatile uint32_t APB1RSTR;
	volatile uint32_t APB2RSTR;
	volatile uint32_t RESERVED1[2];
	volatile uint32_t AHB1ENR;
	volatile uint32_t AHB2ENR;
	volatile uint32_t AHB3ENR;
	volatile uint32_t RESERVED3;
	volatile uint32_t APB1ENR;
	volatile uint32_t APB2ENR;
	volatile uint32_t RESERVED4[2];
	volatile uint32_t AHB1LPENR;
	volatile uint32_t AHB2LPENR;
	volatile uint32_t AHB3LPENR;
	volatile uint32_t RESERVED5;
	volatile uint32_t APB1LPENR;
	volatile uint32_t APB2LPENR;
	volatile uint32_t RESERVED6[2];
	volatile uint32_t BDCR;
	volatile uint32_t CSR;
	volatile uint32_t RESERVED7[2];
	volatile uint32_t SSCGR;
	volatile uint32_t PLLI2SCFGR;
	volatile uint32_t PLLSAICFGR;
	volatile uint32_t DCKCFGR;
	volatile uint32_t CKGATENR;
	volatile uint32_t DCKCFGR2;
}RCC_Regdef_t;

typedef struct
{
	__vo uint32_t  MEMRMP;
	__vo uint32_t  PMC;
	__vo uint32_t  EXTICR[4];
	uint32_t RESERVED1[2];
	__vo uint32_t  CMPCR;
	uint32_t RESERVED2[2];
	__vo uint32_t  CFGR;
}SYSCFG_RegDef_t;


typedef struct
{
	__vo uint32_t IMR;
	__vo uint32_t EMR;
	__vo uint32_t RTSR;
	__vo uint32_t FTSR;
	__vo uint32_t SWIER;
	__vo uint32_t PR;

}EXTI_RegDef_t;

// peripheral definitions

#define GPIOA		((GPIO_RegDef_t*) GPIOA_BASEADDR)
#define GPIOB		((GPIO_RegDef_t*) GPIOB_BASEADDR)
#define GPIOC		((GPIO_RegDef_t*) GPIOC_BASEADDR)
#define GPIOD		((GPIO_RegDef_t*) GPIOD_BASEADDR)
#define GPIOE		((GPIO_RegDef_t*) GPIOE_BASEADDR)
#define GPIOF		((GPIO_RegDef_t*) GPIOF_BASEADDR)
#define GPIOG		((GPIO_RegDef_t*) GPIOG_BASEADDR)
#define GPIOH		((GPIO_RegDef_t*) GPIOH_BASEADDR)

#define RCC 		((RCC_Regdef_t*) RCC_BASEADDR)
#define EXTI  	((EXTI_RegDef_t*) EXTI_BASEADDR)
#define SYSCFG 	((SYSCFG_RegDef_t*) SYSCFG_BASEADDR)

#define GPIOA_CLK() (RCC->AHB1ENR |= (1U << 0))
#define GPIOB_CLK() (RCC->AHB1ENR |= (1U << 1))
#define GPIOC_CLK() (RCC->AHB1ENR |= (1U << 2))
#define GPIOD_CLK() (RCC->AHB1ENR |= (1U << 3))
#define GPIOE_CLK() (RCC->AHB1ENR |= (1U << 4))
#define GPIOF_CLK() (RCC->AHB1ENR |= (1U << 5))
#define GPIOG_CLK() (RCC->AHB1ENR |= (1U << 6))
#define GPIOH_CLK() (RCC->AHB1ENR |= (1U << 7))

#define I2C1_CLK() (RCC->APB1ENR |= (1U << 21))
#define I2C2_CLK() (RCC->APB1ENR |= (1U << 22))
#define I2C3_CLK() (RCC->APB1ENR |= (1U << 23))

#define SPI1_CLK() (RCC->APB2ENR |= (1U << 12))
#define SPI2_CLK() (RCC->APB1ENR |= (1U << 14))
#define SPI3_CLK() (RCC->APB1ENR |= (1U << 15))
#define SPI4_CLK() (RCC->APB2ENR |= (1U << 13))

#define USART1_CLK() (RCC->APB2ENR |= (1 << 4))
#define USART2_CLK() (RCC->APB1ENR |= (1 << 17))
#define USART3_CLK() (RCC->APB1ENR |= (1 << 18))
#define UART4_CLK() (RCC->APB1ENR |= (1 << 19))
#define UART5_CLK() (RCC->APB1ENR |= (1 << 20))
#define USART6_CLK() (RCC->APB2ENR |= (1 << 5))

#define SYSCFG_CLK() (RCC->APB2ENR |= (1 << 14))

#define GPIOA_CLK_DI() (RCC->AHB1ENR &= ~(1U << 0))
#define GPIOB_CLK_DI() (RCC->AHB1ENR &= ~(1U << 1))
#define GPIOC_CLK_DI() (RCC->AHB1ENR &= ~(1U << 2))
#define GPIOD_CLK_DI() (RCC->AHB1ENR &= ~(1U << 3))
#define GPIOE_CLK_DI() (RCC->AHB1ENR &= ~(1U << 4))
#define GPIOF_CLK_DI() (RCC->AHB1ENR &= ~(1U << 5))
#define GPIOG_CLK_DI() (RCC->AHB1ENR &= ~(1U << 6))
#define GPIOH_CLK_DI() (RCC->AHB1ENR &= ~(1U << 7))

#define I2C1_CLK_DI() (RCC->APB1ENR &= ~(1U << 21))
#define I2C2_CLK_DI() (RCC->APB1ENR &= ~(1U << 22))
#define I2C3_CLK_DI() (RCC->APB1ENR &= ~(1U << 23))

#define SPI1_CLK_DI() (RCC->APB2ENR &= ~(1U << 12))
#define SPI2_CLK_DI() (RCC->APB1ENR &= ~(1U << 14))
#define SPI3_CLK_DI() (RCC->APB1ENR &= ~(1U << 15))
#define SPI4_CLK_DI() (RCC->APB2ENR &= ~(1U << 13))

#define USART1_CLK_DI() (RCC->APB2ENR &= ~(1 << 4))
#define USART2_CLK_DI() (RCC->APB1ENR &= ~(1 << 17))
#define USART3_CLK_DI() (RCC->APB1ENR &= ~(1 << 18))
#define UART4_CLK_DI() (RCC->APB1ENR &= ~(1 << 19))
#define UART5_CLK_DI() (RCC->APB1ENR &= ~(1 << 20))
#define USART6_CLK_DI() (RCC->APB2ENR &= ~(1 << 5))

#define SYSCFG_CLK_DI() (RCC->APB2ENR &= ~(1 << 14))

#define GPIOA_REG_RESET() do{(RCC->AHB1RSTR |= (1 << 0)); 			(RCC->AHB1RSTR &= ~(1 << 0));}while(0)
#define GPIOB_REG_RESET() do{(RCC->AHB1RSTR |= (1 << 1)); 			(RCC->AHB1RSTR &= ~(1 << 1));}while(0)
#define GPIOC_REG_RESET() do{(RCC->AHB1RSTR |= (1 << 2)); 			(RCC->AHB1RSTR &= ~(1 << 2));}while(0)
#define GPIOD_REG_RESET() do{(RCC->AHB1RSTR |= (1 << 3)); 			(RCC->AHB1RSTR &= ~(1 << 3));}while(0)
#define GPIOE_REG_RESET() do{(RCC->AHB1RSTR |= (1 << 4)); 			(RCC->AHB1RSTR &= ~(1 << 4));}while(0)
#define GPIOF_REG_RESET() do{(RCC->AHB1RSTR |= (1 << 5)); 			(RCC->AHB1RSTR &= ~(1 << 5));}while(0)
#define GPIOG_REG_RESET() do{(RCC->AHB1RSTR |= (1 << 6)); 			(RCC->AHB1RSTR &= ~(1 << 6));}while(0)
#define GPIOH_REG_RESET() do{(RCC->AHB1RSTR |= (1 << 7)); 			(RCC->AHB1RSTR &= ~(1 << 7));}while(0)

static inline uint8_t GPIO_BASEADDR_TO_CODE(GPIO_RegDef_t *pGPIOx) {
	return ((uint32_t)pGPIOx - 0x40020000) / 0x400;
}

#define ENABLE 1
#define DISABLE 0
#define SET ENABLE
#define RESET DISABLE
#define GPIO_PIN_SET SET
#define GPIO_PIN_RESET RESET

#endif /* INC_STM32F446XX_H_ */
