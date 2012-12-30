HelloWorld: electricImp with Seeedstudio NFC shield
====================================================
- Author: Javier Montaner (@tumaku_ https://twitter.com/tumaku_)
- Date: 30 Dec 2012



Description
---------------
This code initialises SeeedStudio's NFC shield from electricImp using SPI (PINs 2/5/7 plus select PIN 1) and then enters an infinite loop (repeated every X seconds) to detect when a card is presented to the NFC reader. 
When a card is detected, its identity is read and shown in the server. 
The code is based on a similar Arduino example.

Components
-----------
- electricImp: https://www.sparkfun.com/products/11395
- electricImp breakout: https://www.sparkfun.com/products/11400
- SeeedStudio NFC shield: http://www.seeedstudio.com/depot/nfc-shield-p-916:23ce1851341ec1fa9e0c259de10bf87c.html
- MiniUSB cable
- Jumper Wires

Connections
------------
Please take care to connect all the wires correctly to avoid malfunctioning

    electricImp Breakout    SeeedStudio NFC Shield     Function
     GND                     GND                        Ground
     3V3                     5V                         Vcc (note that it is connected to the 5V PIN in the shield!!!)
     PIN1                    PIN10                      Chip Select SPI
     PIN2                    MISO (in ICSP connector)   MISO in SPI
     PIN5                    SCK (in ICSP connector)    Clock in SPI
     PIN7                    MOSI (in ICSP connector)   MOSI in SPI

Additionally connect the 5V PIN in the NFC shield with the VCC PIN in the ICSP connector of the shield

Finally power the electricImp breakout board through the miniUSB cable

Acknowledgements
----------------
Many thanks to Hugo (electricImp) who has provided patient support and useful hints to integrate the SPI protocol between eImp and NFC shield

License 
--------
Copyright 2012 Javier Montaner

The PN532 library is based on the Arduino library produced by SeeedStudio which originates from a previous work of adafruit/ladyada and is licensed under the MIT license.

The rest of the files and work in this project are licensed under the Creative Commons Attribution-ShareAlike 3.0 Unported License. 
To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/3.0/ or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.
