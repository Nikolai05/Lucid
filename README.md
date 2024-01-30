# Lucid
# Let's make a weather sensor with live infomation and Arduino
## Introduction
In this article I’ll be guiding you through the process of connecting your ESP8266 to a live weather service in order to be able to display that on a screen.<br>
```html //#f03c15``` Disclaimer! The information in this article shoudn't be used as a proper manual. Consider this as documentation of my thinking proces with some helpfull tips and tricks.
### Only using Node MCU and internet
To acomplish this goal I can only make use of the Node MCU and internet to simulate a weather sensor.
While looking for information online I realised most of the solutions for weather forecast are using rain sensors, humidity sensors and barometric sensors.
So in order to make this work I had to use a weather API to connect to the Arduino.

## How to make Arduino collect information online and display it in Serial monitor
To learn how to do this, I searched online this exact question. This is what I found:
https://www.instructables.com/Make-ESP8266-Weather-Station/

## Required hardware
1. Node MCU (ESP8266)
<img width="198" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/NodeMcu.jpg">
2. USBc cable
<img width="198" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/usbc.avif">

## Prepare Arduino IDE for ESP8266
### In case you haven't, install Arduino IDE. Once you have done that you can continue with these instructions.
#### The ESP8266 module isn't part of the Arduino-IDE. So we got to install it first.
1. Go to file and select preferences.
2. Adding ESP8266 Board Manager:<br>
   2.1. In the Additional Boards Manager enter the following URL---> http://arduino.esp8266.com/stable/package_esp8266com_index.json<br>
   2.2. Press the OK button.<br>
<img width="400" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/preferences.PNG">
3. Now open the tools in that select Board: “Arduino/Genuino Uno” and click on the Boards Manager. The Boards Manager window opens, scroll to the bottom of the window page till you see the module with the name ESP8266. Select that module and select a version, then click on the Install button. When it is installed it shows Installed in the module.<br>
4. To run the esp8266 with Arduino we have to select the Board: esp8266 modules depending on what you have .This can be done by scrolling down.<br>
5. Now Let’s connect the ESP8266 module to your computer through USB cable as shown in the figure. When module is connected to the USB, COM port will get detected.
<img width="198" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/Connectedpc.jpg">
6. Now open the File tab, go to the Examples, go into Built-in example, go into "01.Basics" and select Blink to open the window.<br>
7. The Blink example will open on a new window , click on tools to select the port: “COM”, based on which esp8266 module is connected to your respected COM port of the computer.<br>
8. Upload the program to the module as shown in figure below. This will start blinking the on board led on the nodemcu module.
<img width="400" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/Uploaded.PNG">
9. You have succesfully tested your ESP8266 and connected it to the Arduino.

## Generating API with Weather information service
1. Go to OpenWeatherMap (https://home.openweathermap.org/)
<img width="400" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/OWMhome.PNG">
2. Create an account.<br>
3. Get account verified.<br>
4. Go to profile and click on "My API keys" as shown in figure below.
<img width="400" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/profile.PNG">
5. Copy API key and paste in some document for later.
<img width="400" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/APIopenweather.PNG">

## Code for Arduino to connect Weather Station 
### Below is the code for IoT Weather Station with NodeMCU OLED & OpenWeatherMap. 
You will need 4 different libraries for that: Adafruit_GFX.h, Adafruit_SSD1306.h, OpenWeatherOneCall.h and ArduinoJson.h. You can get all these libraries from the Library Manager as shown in the figure below. Find them and install them.<br>
<img width="198" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/librarymanager2.PNG">
### Let's get to configuring
1. Go to the following link and copy the entire code (https://github.com/ThingPulse/esp8266-weather-station/blob/master/examples/OpenWeatherMapOneCallDemo/OpenWeatherMapOneCallDemo.ino)
2. Create a file in Arduino and paste the code.
3. Inside Enter your WIFI SSID, Password as show in figure below.
<img width="400" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/enterwifiandssid.PNG">
4. Then add the coordinates of your city. You can go to this adress and enter name of city you want coordinates from. The site wil generate a latitude and longitude.
<img width="400" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/getcoordinates.PNG">
5. Copy them and enter them in the file as shown in figure below.
<img width="400" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/Entercoordinates.PNG">
6. Also add the API key you copied from OpenWeatherMap as show in figure below.
<img width="400" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/Entercoordinates.PNG">
7. Now you can upload this code to NodeMCU Board as shown figure below.
<img width="400" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/uploadcode.PNG">

### Error shown in output when uploading code
When uploading the previous code the following error was given.
<img width="500" alt=image src="https://github.com/Nikolai05/Lucid/blob/main/Erroruploadcode.PNG">
Clearly the output indicates that the library JsonListener.h is missing.
So we are going to go to library manager and install it.
Apparently this library doesn't seem to exist as show in figure below. So we are going to do some online reasearch.

 
