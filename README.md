#Adafruit SPI FRAM Driver #

This driver is (NOT!) for the Adafruit SPI FRAM Breakout (at the moment)
    ------> http://www.adafruit.com/products/1897

    This library was forked from Adafruit's SPI FRAM Breakout driver github
repository.  Because I use an 8-DIP 2Mbit Fujitsu FRAM chip in one of my
projects, I have attempted to modify Adafruit's library to talk to these
much larger chips.  The 2Mbit chip requires the use of a 24-bit (technically
it only uses 18 bits of those 24) address, so I have changed the uint16_t
addr variable to an unsigned long (32 bits) and added logic to extract the
three required bytes to be sent over SPI to the FRAM chip.
    In the future, I will try to add logic to test the chip for size and
send the appropriate number of address bytes rewuired for the chip being
used if this is possible.

## About this Driver ##

These modules use SPI to communicate, 4 pins are required to  
interface

Adafruit invests time and resources providing this open source code,
please support Adafruit and open-source hardware by purchasing
products from Adafruit!

Written by Kevin (KTOWN) Townsend for Adafruit Industries.
BSD license, check license.txt for more information
All text above must be included in any redistribution

To download. click the ZIP button in the top bar, and check this tutorial
for instructions on how to install:
http://learn.adafruit.com/adafruit-all-about-arduino-libraries-install-use
