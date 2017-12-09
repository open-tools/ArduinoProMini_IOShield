# ArduinoProMini_IOShield

Breakout board for Arduino Pro Mini with interface for NRF24L01+ and RFM69H wireless modules and breadboards and/or I²C connectors

This board is inspired by the Arduino "Nano IO Shields" available for cheap at aliexpress (search for "arduino nano nrf24l01 board", e.g. [here](https://www.aliexpress.com/item/Free-shipping-Nano-328P-IO-wireless-sensor-expansion-board-for-XBEE-and-NRF24L01-Socket-for-arduino/32298692903.html)), which provide breakout pins for each analog and digital pin (each with its own VCC+GND pins), a connector for an NRF24L01+ module and an XBee module. Furthermore, these boards have their own voltage regulators with a 5.5x2.1mm power jacks (for 6-12V input), so VCC for the output pins does not have to go through the arduino.
As I don't have any use for the XBee socket, I simply broke off the header pins and instead taped a [tiny 5x11 pin breadboard](https://www.aliexpress.com/item/7Pcs-Mini-55-Points-Breadboard-Solderless-Prototype-Tie-point-For-Arduino-GM/32670910749.html) to the board, which I typically use to attach multiple I²C sensors. 

These boards are perfect for quick prototyping for the MySensors project for several reasons:
* you have the nrf24l01+ radio module already wired with their own voltage regulators and level shifters
* The board has its own power input and voltage regulators (VCC 5V will be fed to the Nano), so sensors with a high current requirement will get the power directly from the supply and not through the Arduino board.
* Each analog and digital pin has its own VCC+GND pins (usually when working with multiple sensors there is a severe shortage of VCC/GND pins for each sensor)
* The I²C and serial (RX/TX) lines are readily available as 1x4 pin headers (i.e. you don't need to know whether A4 or A5 is SDA or SCL).


The only drawback is that I use Pro Minis for most of my projects, so prototyping with a Nano means you are never testing the actual board in the prototype.


