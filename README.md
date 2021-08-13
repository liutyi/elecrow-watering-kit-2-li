# Custom Firmware for Elecrow Watering Kit 2.1

I purchased the [Elecrow Watering Kit 2.1](https://www.elecrow.com/arduino-automatic-smart-plant-watering-kit.html)
from [Amazon](https://www.amazon.com/Elecrow-Watering-Moisture-Gardening-Automatic/dp/B07LCNKC6N). 
The controller board for this kit has an integrated
Arduino Leonardo.

The included firmware (and the firmware found on the Elecrow site) has issues, notably graphical gitches. I've included a copy of the Elecrow code in the `orig/` folder for comparison purposes.

I found a [version of the firmware](https://github.com/liutyi/elecrow-watering-kit-2-li)
modified by [liutyi](https://wiki.liutyi.info/display/ARDUINO/Arduino+Automatic+Smart+Plant+Watering+Kit+2.0a) 
that fixed these gitches. 

As I plan on expanding upon this code, I've refactored the code so it doesn't repeat itself four times every time it does something.

TODO
---------
* Support a depth sensor for the water. I plan to add support for the VL53L0X Time-of-Flight (ToF) Laser Ranging Sensor I2C IIC module.
* Supply sensor and pump data over RX/TX to an ESP32 or ESP8266.
* Code on the ESP32/ESP8266 to read the sensor data and publish it to a local MQTT (Mosquitto) broker so I can use Grafana to visualize
