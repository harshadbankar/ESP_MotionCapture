# ESP Motion Capture
Motion capturing and its translation to a virtual object through cloud using ESP8266 and MPU6050 sensor.Also has a feature to perform OTA update

## Essential changes
1) Download the ESP8266httpUpdate.cpp file and replace the existing file available at  
> ..\packages\esp8266\hardware\esp8266\2.3.0\libraries\ESP8266httpUpdate\src

This change helps us to publish the status of FOTA to cloudmqtt before the ESP restarts

2)Replace 
```
#include <avr/pgmspace.h> 
```
with 
```
 #include <avr/pgmspace.h>
 #else
 #include <pgmspace.h>
 #endif
```
in the following files: MPU6050.h, MPU6050_6Axis_MotionApps20.h, MPU6050_9Axis_MotionApps41.h
This change is necessary to port MPU6050 arduino library to ESP8266

## Working prototype video
https://www.youtube.com/watch?v=onj2CMYKwHU 
## Project Description
Please read wiki for explanation of the project
