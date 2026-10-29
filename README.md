# VRS – Zadanie 5

Aplikácia pre STM32F303K8 (Nucleo-32) so senzorovou doskou X-NUCLEO-IKS01A1.
Zo senzorov HTS221 (teplota, vlhkosť) a LPS25HB (tlak) cez I2C číta údaje
a posiela ich cez USART2 vo formáte CSV do PC (Serial Oscilloscope).

## Periférie
- I2C1: PB6 – SCL, PB7 – SDA
- USART2: PA2 – Tx, PA15 – Rx, 115200 baud, DMA1 kanál 6/7
- LED: PB3

## Formát odosielaných dát
`teplota [°C],vlhkosť [%],tlak [hPa],relatívna výška [m]` – napr. `23.4,45,1013.25,0.52`
