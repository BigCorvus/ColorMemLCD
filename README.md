# ColorMemLCD
Arduino library for the LPM013M126A 176x176 Japan Display 8-Color memory LCD, found inside the SMA-Q2 / SMA-TIME smartwatch.  Only tested on the Adafruit nrf52832 core 0.8.5 for Arduino, which is able to run on this watch.

The ColorMemLCD library is based on the mbed library for the JDI 3bit-color memory LCD LPM013M126A
by Tadayuki Okamoto, originally released under the MIT License as well as the Adafruit library for the SHARP memory LCDs. It relies on the Adafruit GFX library for graphics functions.

Uses hardware SPI on the nrf52832 and an external signal for the EXTCOMIN (P0.06). I just left the AVR softSPI functions untouched but the library has not been tested on AVR!
By default the EXTMODE pin of the display is set HIGH via a 10k resistor, 
which means that the display expects toggling this pin from time to time (at least
once per minute, see datasheet). 
This example is based on the sharpmemtest.ino by Adafruit an relies on the Adafruit GFX library. 


