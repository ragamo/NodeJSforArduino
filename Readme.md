NodeJS for Arduino
==================

Source: http://giorgiocefaro.com/blog/installing-node-js-on-arduino-yun

NodeJS compiled by Nikola Gluhovic (version 0.10.20 with SSL support)


How to Install on Arduino
-------------------------

Copy packages to your Yún:

	$ scp *.ipk root@myArduinoaddress:/tmp

Access to your Arduino via SSH and install the packages:

	$ opkg install /tmp/uclibcxx_0.2.4-1_ar71xx.ipk
	$ opkg install /tmp/node_v0.10.20_ar71xx.ipk
	

Test
----

For test the installation, execute:

	$ node
	> 1+1


Usage
-----

Now you can execute Node process in your sketchs:

	Process node;
  	node.begin("node");
 	node.addParameter("/node/index.js");
  	node.run();
	
	while(node.available() > 0) {
		char c = node.read(); 
		Serial.print(c);
	}
	

Experiments
-----------
Some experiments here: https://github.com/ragamo/ArduinoLab
