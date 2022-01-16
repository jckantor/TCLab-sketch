TCLab-sketch
============

TCLab-sketch repository is a set of Arduino sketches which, when downloaded and installed
on a compatible Arduino device, supports the 
[Temperature Control Lab](http://apmonitor.com/pdc/index.php/Main/ArduinoTemperatureControl). 
The sketch is used in conjunction with the compatible Python library 
[TCLab](https://github.com/jckantor/TCLab) for programmable control of the Temperature
Control Lab with Python. There are three versions of the sketch:

* **TCLab-sketch** Provides access to the TCLab via Python Serial library.
* **TClab-sketch-webusb** Developmental version for WebUSB access.
* **TCLab-sketch-vocareum** Developmental version for Vocareum using WebUSB access.


Hardware setup
--------------

1. Plug the Temperature Control Laboratory shield in an Arduino UNO or Leonardo. Connect your computer
   to the Arduino via the USB connection. Plug the DC power adapter into the wall  and attach to the 
   power input to the Temperature Control Laboratory sheid.

2. Install Arduino Drivers if needed. For most users there will be no need. If you are using Windows 10 the Arduino board should connect with no additional drivers. Mac OS users may need to install a serial driver for old models of the Temperature Control that used Arduino Uno clones. For clones using the CH340G, CH34G or CH34X chipset, a suitable driver can be found 
   [here](https://github.com/MPParsley/ch340g-ch34g-ch34x-mac-os-x-driver>)
   or
   [here](https://github.com/adrianmihalko/ch340g-ch34g-ch34x-mac-os-x-driver)

3. Install Arduino Firmware

   * Download and install the [Arduino IDE](https://www.arduino.cc/en/Main/Software) application.
   * Download the file TCLab-sketch.ino located in this repository in the folder with the same name.
   * Open the Arduino IDE application. From the Tools menu, select the Arduino board type and 
     verify the port connection.
    * Compile and upload TCLab-sketch.ino
   
4. Test

   Use the serial monitor (located under the tools menu of the Arduino IDE) to confirm operation. 
   Select serial monitor, set baud rate to 9600 and line endings to 'newline'. If the firmware is
   operating correctly, entering the command
   
       LED 100
       
   will cause the LED to flash at 100% power for 10 seconds.
