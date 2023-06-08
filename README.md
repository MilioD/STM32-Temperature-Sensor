# STM32 NUCLEO-F446RE Bare Metal Temperature Sensor

Bare metal register-level TMP37 temperature sensor interface using the STM32 NUCLEO-F446RE board

The ADC peripheral performs its conversions on an external event trigger (TIM2 TRGO). I am using ADC1 channel 0 to convert the analog data read from the analog temperature sensor (TMP37) connected to the pin PA0 (ADC1_IN0).

The ADC is using DMA mode to transfer the converted temperature data to a memory location, from where it can then be read. To perform this peripheral-to-memory transfer, I am using DMA2 Stream 0.
