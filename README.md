# Remote control Daikin heatpump
Based on the work of iproDIY (https://youtu.be/JT0u7wrnaT4?si=S1c3XjLaEUnJjGbb) . 
Since I have two different Daiking heatpumps i needed to make two solutions

Hardware:
- Infrared Transceiver ESP8285 Wireless Transceiver Module WIFI Remote Control Switch Development Learning Board (https://www.icstation.com/infrared-transceiver-esp8285-wireless-transceiver-module-wifi-remote-control-switch-development-learning-board-p-14369.html)
- Wiring

Description:
The internal solution takes power at IR reciever from the heatpump board. The ESP reads the signal and send this to Home Assistant. Home Assistant updates according to Daikings remote control. If you change values in Home Assistant, the board transmits IR signal to the heatpump.

The external solution need power from f.ex a USB charger. The ESP reads the signal and send this to Home Assistant. Home Assistant updates according to Daikings remote control. If you change values in Home Assistant, the board transmits IR signal to the heatpump.



Configuration:
- Change "delay" to the value your garagedoor uses to close or open. Any time over this limit results in error in Home Assistant.

For internal power of IR Reciever, use the daikin-internal.yaml, and connect the board to Daiking heatpump according to the Youtube video

For external power IR Reciever, use the daikin-external.yaml, and place the board over the reciever panel on the heatpump.