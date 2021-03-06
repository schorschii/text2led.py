text2led.py
===========

This is a python script to control led display boards also known as led bars or led ticker via serial or usb connection.

The script works at least with following displays:
- Skytronic MSB-67 / 153.141
- Velleman MML16CN 
- AM004-03127 (the Conrad Laufschrift)

Please inform me, if it also works with other models.

The core class is taken from:
http://gathering.tweakers.net/forum/list_message/30160421#30160421

How to use
----------

The script offers three modi operandi:

- Manual: The script waits for input via the cmd line.

- iTunes: The script uses AppleScript to poll ITunes every second for current song's name and artist. Only on OSX

- VirtualDJ: The script checks every second the history of the DJ program VirtualDJ for new entries and outputs the last entrie's song name and artist. Tested on Windows7 and OSX. 

Each one of the three modi is activate by commenting out the other two. Please look at the function for further details.
    
Preparations:
-------------

1. find out the right serialport
  1. for Windows it is "\\.\COM3" in my experince
  2. for Mac OSX it is "/dev/cu.SLAB_USBtoUART"
  3. For OSX you first have to install the USB2Serial driver. I used:  http://www.silabs.com/products/mcu/Pages/USBtoUARTBridgeVCPDrivers.aspx
2. edit the serial port, see __main__

How to change display options:
------------------------------

The display options can be changed via the settings variable.
All the different supported options can be found in the documentation of the led display boards. Copies can be found here:
- http://www.produktinfo.conrad.com/datenblaetter/575000-599999/590998-da-01-en-LED_LAUFSCHRIFT_ROT.pdf
- http://www.domotiga.nl/attachments/39/RGB_ledbar_conrad.pdf
