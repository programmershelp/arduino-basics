The Arduino Uno is based on an ATmega328 microcontroller This board includes 14 digital I/O pins, a power jack, 6 analog input pins, a 16MHz ceramic resonator, a USB connection, a reset button, and an ICSP programming header. 

[![](https://ae01.alicdn.com/kf/HTB1Q_Hsv7yWBuNjy0Fpq6yssXXao/-font-b-UNO-b-font-R3-Development-Board-ATmega328P-CH340-CH340G-For-font-b-Arduino.jpg_350x350.jpg)](https://s.click.aliexpress.com/e/_dUF7OTN)

### Features

|     |     |
| --- | --- |
| **Microcontroller** | ATmega328P |
| **Operating Voltage** | 5V  |
| **Input Voltage (recommended)** | 7-12V |
| **Input Voltage (limit)** | 6-20V |
| **Digital I/O Pins** | 14 (of which 6 provide PWM output) |
| **PWM Digital I/O Pins** | 6   |
| **Analog Input Pins** | 6   |
| **DC Current per I/O Pin** | 20 mA |
| **DC Current for 3.3V Pin** | 50 mA |
| **Flash Memory** | 32 KB (ATmega328P) of which 0.5 KB used by the bootloader |
| **SRAM** | 2 KB (ATmega328P) |
| **EEPROM** | 1 KB (ATmega328P) |
| **Clock Speed** | 16 MHz |
| **LED_BUILTIN** | 13  |

### Arduino Uno Pin Diagram

![](http://www.aboutmicros.com/wp-content/uploads/2020/09/arduino-uno-pinout-diagram.jpg) 

The Arduino Uno board can be built with power pins, analog pins, ATmegs328, ICSP header, Reset button, power LED, digital pins, test led 13, TX/RX pins, USB interface, an external power supply. 

The Arduino UNO board description is discussed below.

### Power Supply

You can power the Arduino Uno with either a USB cable or an external power supply. 

The external power supplies can be a 9v battery or a DC power supply. 

The power supply can be connected to the Arduino Uno by plugging into the power jack of the Arduino board. 

You can also use connect to the Vin pin and the GND pin of the POWER connector. 

The suggested voltage range is 7 volts to 12 volts.

### Input & Output

The 14 digital pins on the Arduino Uno can be used as input & output with the help of the functions like pinMode(), digitalWrite(), & Digital Read(). 

These pins can be configured to work as input digital pins to read logic values (0 or 1) or as digital output pins 

**Pin1 (TX) & Pin0 (RX) (Serial):** 

These pins are used to transmit and receive serial data, and these are connected to the ATmega8U2 USB to TTL Serial chip equivalent pins. 

An example would be a bluetooth board. 

P**in 2 & Pin 3 (External Interrupts):** 

External pins can be connected to activate an interrupt over a low value, change in value. 

**Pins 3, 5, 6, 9, 10, & 11 (PWM):** 

These pins give 8-bit PWM. You can use analogWrite() function for this. 

**SPI Pins (Pin-10 (SS), Pin-11 (MOSI), Pin-12 (MISO), Pin-13 (SCK):** 
These pins are used for SPI communication. There are several sensors and LCDs that use SPI. 

**Pin-13(LED):** 

The inbuilt LED is connected to pin 13. When the output is high, the light-emitting diode is activated. 

**Pin-4 (SDA) & Pin-5 (SCL) (I2C):** 

It supports TWI-communication with the help of the Wire library. You can connect various sensors to these pins 

**AREF (Reference Voltage):** 

The reference voltage is for the analog inputs. You use this with the analogReference() function.  

It is sometimes, used to set an external reference voltage (between 0 and 5 Volts). 

**Reset Pin:** This pin is used for reset (RST) the microcontroller.

### Memory

The memory of the Atmega328 microcontroller includes32kb of flash memory which is used for storing code, 2kb of SRAM and 1kb of EEPROM.

### Communication

The Arduino Uno offers serial communication, and it is accessible on digital pins like TX (1) and RX (0). 

There are two LEDs on the board called RX and TX which will blink whenever data is being sent through the USB. 

A SoftwareSerial library permits for serial communication on Arduino Uno digital pins and the ATmega328P supports I2C  as well as SPI-communication.
