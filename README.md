# Lucid
# Let's make a weather sensor with live infomation and Arduino
## Only using Node MCU and internet
To acomplish this goal I can only make use of the Node MCU and internet to simulate a weather sensor.
While looking for information online I realised most of the solutions for weather forecast are using rain sensors, humidity sensors and barometric sensors.
So in order to make this work I had to use a weather API to connect to the Arduino.

## How to make Arduino collect information online and display it in Serial monitor
To learn how to do this, I searched online this exact question. This is what I found:
https://www.instructables.com/Make-ESP8266-Weather-Station/

## Required hardware
1. Node MCU (ESP8266)
<img width="198" alt=image src="https://github.com/Nikolai05/IoT3/blob/main/NodeMcu.jpg">
2. USBc cable
<img width="198" alt=image src="https://github.com/Nikolai05/IoT3/blob/main/usbc.avif">

## Weather information service
1. Go to OpenWeatherMap (https://home.openweathermap.org/)
2. Create an account
3. Get account verified
4. Copy API key

## Prepare Arduino IDE for ESP8266
### In case you haven't, install Arduino IDE. Once you have done that you can continue with these instructions.
1. Go to file and select preferences.
2. Adding ESP8266 Board Manager:
   2.1. In the Additional Boards Manager enter the following URL---> http://arduino.esp8266.com/stable/package_esp8266com_index.json
   2.2. Press the OK button.
3. Now open the tools in that select Board: “Arduino/Genuino Uno” and click on the Boards Manager. The Boards Manager window opens, scroll to the bottom of the window page till you see the module with the name ESP8266. Select that module and select a version, then click on the Install button. When it is installed it shows Installed in the module.
4. To run the esp8266 with Arduino we have to select the Board: “Arduino/Genuino Uno” and then change it to NodeMCU 1.0 (ESP-12E Module) or other esp8266 modules depending on what you have .This can be done by scrolling down.
5. Now Let’s connect the ESP8266 module to your computer through USB cable as shown in the figure. When module is connected to the USB, COM port will get detected.
6. Now open the File tab, go to the Examples, go into Built-in example, go into "01.Basics" and select Blink to open the window.
7. The Blink example will open on a new window , click on tools to select the port: “COM”, based on which esp8266 module is connected to your respected COM port of the computer.
8. On the blink example code change all number 13 to number 16 and then click on the right arrow shown in the figure to upload the program to the module. This will start blinking the on board led on the nodemcu module.
9. You have succesfully tested your ESP8266 and connected it to the Arduino.

##


 
