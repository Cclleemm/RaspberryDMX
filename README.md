RaspberryDMX
===================
Raspberry Pi HTTP to GPIO DMX

This is an experimental tool to create a cheap DMX controller with your Raspberry Pi. It only cost the price of your raspberry pi and the MAX485 RS-485 Module (around 2$).
This script will help you to create a way to control DMX device through a web HTTP page.

----------

What you need ?
-------------

Item         				| Value
----------------------------| ---
Raspberry Pi 				| ![PreviewImage](https://raw.github.com/Cclleemm/RaspberryDMX/master/Tutorial/raspberry.png?raw=true) 
MAX485 RS-485 Module   	 	| ![PreviewImage](https://raw.github.com/Cclleemm/RaspberryDMX/master/Tutorial/max485.png?raw=true) 
Cable   		 			  | ![PreviewImage](https://raw.github.com/Cclleemm/RaspberryDMX/master/Tutorial/cable.png?raw=true) 
Some 0.1 pin header cables	| ![PreviewImage](https://raw.github.com/Cclleemm/RaspberryDMX/master/Tutorial/pins.png?raw=true) 
Plug suitable for DMX (XLR)	| ![PreviewImage](https://raw.github.com/Cclleemm/RaspberryDMX/master/Tutorial/dmxplug.png?raw=true) 


----------

First step
-------------
the Raspberry Pi (rpi) is not 5volt tolerant (it does not accept 5v inputs) but the module has pull-up resistors on the I/O lines pulling the logic signals up to 5v. These resistors need to be removed otherwise damage may result to the rpi, things may get hot, smell bad at best or fail completely at worst.
So take your soldering iron to remove resistors. 
**If you don't, it can damage your Raspberry Pi**.



Before         				| After
----------------------------| ---
![PreviewImage](https://raw.github.com/Cclleemm/RaspberryDMX/master/Tutorial/max485_2.png?raw=true)  				| ![PreviewImage](https://raw.github.com/Cclleemm/RaspberryDMX/master/Tutorial/max485_3.png?raw=true) 


----------


Second step
-------------
Now you need to connect the MAX485 board to the GPIOs of the Raspberry Pi.
Follow the connection picture. 

![PreviewImage](https://raw.github.com/Cclleemm/RaspberryDMX/master/Tutorial/board.png?raw=true) 

> **Note:**

> - The RO pin is optional.
> - The DE pin have to be connected on the GPIO21 or GPIO27 (it depends of the RBPi version).


Third step
-------------
Wire the MAX485 board to the DMX plug (XLR 3pins) or socket.

Wire         				| Result
----------------------------| ---
**B** is positive (red) and goes to **pin 3** on the socket. **A** is negative (black) and goes to **pin 2**.   				| ![PreviewImage](https://raw.github.com/Cclleemm/RaspberryDMX/master/Tutorial/plugconnected.png?raw=true) 


Image is socket viewed from back. 
