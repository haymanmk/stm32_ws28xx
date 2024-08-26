# STM32 Controls WS28XX with PWM
This project is dedicated on controlling WS28XX RGB LED strip/matrix with PWM.
## Protocol
For the detailed information, please refer to [WS2812 manual](Doc/WS2812.pdf).
## DMA
Circular mode is introduced here, and the buffer is devided into 2 halves, first half updated in half transfer complete ISR and last half updated in full transfer complete ISR. 
- Circular Mode
- Half Trandfer Complete: trigger ISR to update first half of a buffer
- Full Tansfer Complete: trigger ISR to update last half of a buffer