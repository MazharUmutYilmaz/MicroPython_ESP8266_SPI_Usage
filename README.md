# MicroPython_ESP8266_SPI_Usage
SPI Usage with MAX7219 DOT Matrix Module on ESP8266 with MicroPython

import max7219
from machine import Pin, SPI
spi = SPI(1, baudrate=10000000, polarity=0, phase=0)
screen = max7219.Matrix8x8(spi, Pin(15), 1)
screen.brightness(5)
screen.fill(0)
screen.text('3',0,0,1)
screen.show()

