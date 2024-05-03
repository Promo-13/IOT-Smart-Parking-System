# IOT-Smart-Parking-System
This is an IOT based smart parking system.

# Components Required
## Hardware

NodeMCU ESP8266 <br>
IR Sensor (5) <br>
Servo Motor (2) <br>
## Online Services

Adafruit IO

# Adafruit IO Setup for IOT Parking System
Adafruit IO is an open data platform that allows you to aggregate, visualize, and analyze live data on the cloud. Using Adafruit IO, you can upload, display, and monitor your data over the internet, and make your project IoT enabled. You can control motors, read sensor data, and make cool IoT applications over the internet using Adafruit IO. For test and try, with some limitation, Adafruit IO is free to use. We have also used Adafruit IO with Raspberry Pi previously.

1. To use Adafruit IO, first, you have to create an account on Adafruit IO. To do this, go to the Adafruit IO website and click on ‘Get started for Free’ on the top right of the screen.
2. After finishing the account creation process, log in to your account and click on ‘AIO Key’ on the top right corner to get your account username and AIO key.When you click on ‘AIO Key,’ a window will pop up with your Adafruit IO AIO Key and username. Copy this key and username, it will be needed later in the code.
3. Now, after this, you need to create a feed. To create a feed, click on ‘Feed.’ Then click on ‘Actions,’ and then on ‘Create a New Feed’ as shown in the image below.
4. After this, a new window will open to enter the Name and Description of the feed. The writing description is optional.
5. Click on ‘Create,’ after this; you will be redirected to your newly created feed. 
For this project, we created a total of nine feeds for exit gate, entry gate, slot 1 entry & exit, slot 2 entry & exit, and slot 3 entry & exit.
After creating feeds, now create an Adafruit IO dashboard to show all of these feeds on a single page. To create a dashboard, click on the Dashboard option and then click on the ‘Action,’ and after this, click on ‘Create a New Dashboard.’
In the next window, enter the name for your dashboard and click on ‘Create.’.
6. As the dashboard is created now, we will add our feeds to the dashboard. To add a feed, click on the ‘+’ in the top right corner.First, we will add two RESET buttons blocks for Entry and Exit gate and then seven TEXT blocks for parking details.
To add a button on the dashboard click on the RESET block.In the next window it will ask you to choose the feed, so click on the entry gate feed.
7.In this step, give your block a title and customize it accordingly. Change the press value from ‘1’ to ‘ON’. So whenever the button is pressed it will send the ‘ON’ string to NodeMCU, and NodeMCU will perform the further task. If you don’t want to change the press value here than you can change the condition in the program.
8.After this, follow the same procedure to create another block for the exit gate.
To create the rest of the blocks follow the same procedure, but instead of creating a RESET block, create a TEXT block so that you can show the parking details.
After creating all the blocks, my dashboard looks like below. You can edit the dashboard by clicking on the settings buttons.

# Programming NodeMCU for IOT Parking System

1. To program NodeMCU with Arduino IDE go to File–>Perferences–>Settings.
2. Enter https:// arduino.esp8266.com/stable/package_esp8266com_index.json into the ‘Additional Board Manager URL’ field and click ‘Ok’.
3. Now go to Tools > Board > Boards Manager.
4. In Boards Manager window, Type esp in the search box, esp8266 will be listed there below. Now select the latest version of the board and click on install.
5. After installation is complete, go to Tools >Board >and select NodeMCU 1.0(ESP-12E Module). Now you can program NodeMCU with Arduino IDE.
6. First, include all the required libraries. ESP8266 Wi-Fi and Servo.h libraries are already installed in the IDE. You can download the NTP client and Adafruit MQTT libraries from the below links.<br>

# Library Links:

Adafruit_MQTT: https://github.com/adafruit/Adafruit_MQTT_Library <br>
NTP_Client : https://github.com/arduino-libraries/NTPClient 


