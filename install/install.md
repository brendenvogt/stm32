# Install
## Overview
Goal: Program the stm32 using various means

The stm32 blue pill might ship with read protection built in from the factory. this causes a lot of headache when trying to program using any means. 


### Disable Read Out Protection
We need to write the following option bytes in order to turn off read data protection
```
RDP=0xA5 
```

## Flashing 
```
cd stm32
st-flash --reset write ./examples/STM32_Blink/STM32_Blink.bin 0x8000000
```
## Flashing Boot Loader
```
st-flash --reset write ./examples/STM32duino/generic_boot20_pc13.bin 0x8000000
```