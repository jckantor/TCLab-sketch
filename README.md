TCLab-sketch
============

TCLab-sketch repository is a set of Arduino sketches which, when downloaded and installed
on a compatible Arduino device, supports the 
[BYU Arduino Temperature Control Lab](http://apmonitor.com/pdc/index.php/Main/ArduinoTemperatureControl). 
The sketch is used in conjunction with the compatible Python library 
[TCLab](https://github.com/jckantor/TCLab) for programmable control of the Temperature
Control Lab using Python. There are three versions of the sketch:

* |TCLab-sketch| Provides access to the TCLab via Python Serial library or WebUSB.
* |TClab-sketch-webusb| Developmental version for WebUSB access.
* |TCLab-sketch-vocareum| Developmental version for Vocareum using WebUSB access.


Hardware setup
--------------

1. Plug the Arduino (UNO or Leonardo) with the lab attached into your computer via the USB connection. 
   Plug the DC adapter into the wall.

2. (optional) Install Arduino Drivers

   *If you are using Windows 10, the Arduino board should connect without additional drivers required.*

   Mac OS X users may need to install a serial driver. For arduino clones using the CH340G, CH34G
   or CH34X chipset, a suitable driver can be found 
   [here](https://github.com/MPParsley/ch340g-ch34g-ch34x-mac-os-x-driver>)
   or
   [here](https://github.com/adrianmihalko/ch340g-ch34g-ch34x-mac-os-x-driver)

3. Install Arduino Firmware

   Flash the board with the custom firmware TCLab-sketch.ino located in the folder with the same name.
   This is done using the [Arduino IDE](https://www.arduino.cc/en/Main/Software).
   
4. Test

   Use the serial monitor (located under the tools menu of the Arduino IDE) to confirm operation. 
   Select serial monitor, set baud rate to 9600 and line endings to 'newline'. If the firmware is
   operating correctly, entering the command
   
       LED 100
       
   will cause the LED to flash at 100% power for 10 seconds.
