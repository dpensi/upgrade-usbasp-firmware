Upgrade usbasp firmware
=======================

This is a small guide on how to upgrade your usbasp firmware using arduino
(only one usbasp required)


Schematics
----------

![schematics](/usbasp-firmware-update-connections.jpg)

Jumper to close
---------------

![jumper](/usbjumper-768x544.png)

Instructions
------------

1. wire your arduino to your usbasp as shown in the schematics above
1. close the jumper highlighted in the picture below the schematics
1. connect your arduino to your pc
1. open the arduino ide and click on 
`File -> Examples -> 11. ArduinoISP -> ArduinoISP`
1. click on `Upload`
1. from the root directory of this repository lunch the following command:
`./avrdude -C ./avrdude.conf -p m8 -c avrisp -P /dev/ttyACM0 -b 19200 -U flash:w:usbasp.atmega8.2011-05-28.hex:i `

**notes:**
* the port (`-P` parameter) may vary according to your system, you can find the 
port by opening the arduino ide and clicking `Tools -> Port`

