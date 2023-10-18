# Lucid
# Let's make a proximity sensor and turn on a light
## Required hardware
1. Node MCU (ESP8266)
   <img width="198" alt=image src="https://github.com/Nikolai05/IoT3/blob/main/NodeMcu.jpg">
3. Ultrasonic sensor (HC-SR04)
   <img width="198" alt=image src="https://github.com/Nikolai05/IoT3/blob/main/NodeMcu.jpg">
5. LED strip with cable
  <img width="198" alt=image src="https://github.com/Nikolai05/IoT3/blob/main/NodeMcu.jpg">
7. USBc cable
  <img width="198" alt=image src="https://github.com/Nikolai05/IoT3/blob/main/NodeMcu.jpg">  
9. Arduino cables
  <img width="198" alt=image src="https://github.com/Nikolai05/IoT3/blob/main/NodeMcu.jpg">  

## Connecting the hardware
### Node MCU to LED strip
<img width="198" alt=image src="https://github.com/Nikolai05/IoT3/blob/main/NodeMcu.jpg">

### Node MCU to Ultrasonic sensor
This link explains how this connection works:
https://mindstormengg.com/nodemcu-esp8266-lab-5-ultrasonic-sensor/
<img width="198" alt=image src="https://github.com/Nikolai05/IoT3/blob/main/NodeMcu.jpg">

## Testing the Ultrasonic sensor
Make sure to have "Arduino_GroveI2C_Ultrasonic.h" installed, if not go to library and install
<img width="198" alt=image src="https://github.com/Nikolai05/IoT3/blob/main/NodeMcu.jpg">
Go to File>Examples>Arduino_GroveI2C_Ultrasonic>simplereading
Open it and upload the code to test.

## Testing LED strip
Go to File>Examples>FastLED and select any of the examples to test.
Open it and upload the code to test.
The idea is that the LED strip lights up slowly to simulate the effect of Lucid when proximity sensor is triggered.


## Why it's not possible to connect both a LED strip and a Ultrasonic grove to a node MCU without an additional D5 pin
The NodeMCU doesn't have enough D5 pins to support both connections.
You could use an Arduino Uno instead.


## This is what I want!
https://www.youtube.com/watch?v=Ny1Lv7a-qJs


 
