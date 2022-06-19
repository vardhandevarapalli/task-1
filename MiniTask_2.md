# [Arduino Nano Quadruped Robot](https://www.instructables.com/Arduino-Nano-Quadruped-Robot/)
## Problem Statement:-
Designing a spider like robot which can do creep gait movement when power is supplied.
## Ideation and Planning:-
understanding the quadruped robots mechanism.
- Portable Power Supply->Microcontroller->Adrduino Expansion shield->Servo Motors 

| Part of the Pipeline | Feasibility | Advantages | Disadvantages |
| :---: | :---: | :---: | :---: |
| Portable Power Supply | easy to find a suitable powersupply but its a bit hard to include the power source inside the smaller designs and to power the projects for longer times  | gives power to the project without a need to connect to external sockets | sometimes Power discharge is irregular and causes the Micro controllers and chipsets to burn or get damaged |
| Microcontroller | Hard for a beginner to understand the Usage of the each Pins and to perfectly write the suitable code for the project  | has many features for making different projects and also has many libraries for the beginners to be able to code properly  | can easily be Damaged with high power supply than required and hard for the beginners to work with |
| Arduino Expansion Shield | it expands the Arduino Microcontroller to link other devices in a simple and trouble-free manner | acts as a breakout board for the Arduino microcontroller and each pinout includes 5V and GND pins for easy connection to sensors or servos | high voltages can cause the expansion shield to damage also parallely damaging the Microcontroller |
| Servo Motors | easy to control and can be customised and controlled  easily  | Angular motion, velocity control can be possible using a servo motor and works on defferent scales of voltage  | high torques makes the servo motors to fail and they are a bit expensive than regular motors |

I personally Do not feel like this project meets the constraints because this can only move forward and can not be controlled properly so i would like to ideate the solution again by changing and adding a few parts to the existing project to get to a better solution to the problem statement.

## Choosing a new pipeline:-
understanding the problem statement clearly to create a new and efficient pipeline.
- Power Supply-> Smartphone app ->Bluetooth Transreciver-> Microcontroller-> Arduino Expansion Shield-> Servo Motors
- there is also a need to re-design the project according to fit all the new components in it and i also think that the existing design has some flaws regarding the design of the legs.

| new parts of the pipeline | Feasibility | Advantages | Disadvantages |
| :---: | :---: | :---: | :---: |
| Replacing the Mophie Juice pack powertstation Pro with two Li-Po 18650 3.7v 2600mAh batteries connected in series along with TP4056 1-cell Li-Ion Charging module | Is feasible as the mentioned components costs lesser the used battery pack and can be fit inside the robots module | battery pack can be recharged at any time and takes less space | we need to use two batteries in series to achieve required voltage |
| Developinng a new Smartphone Apk | hard to code an apk but is feasile as it can be done by using the MIT app inventor | easy to communicate and to control the microcontroller | security issues it  can be hacked easily |
| connecting a Hc05 BLuetooth module| easy to use the module and is feasible as it can be connected to the arduino nano to control the input signals | low power consumption cheaper cost and best for low range communications | lower bandwidth compared to the WIFi |
## Prototyping phase:-
FIrst of all a Prototype which is as shown in the mentioned project be made 
- first by designing the parts using any CAD software like Fusion 360 and to be printed using a PLA Filament or PETG Filamnet - 
- then the parts need to be attached step by step along with the servo motors
- then the according to the schematics mentioned in the projects it needs to be wired and servo motors are also connected accordingly.
- Now using the software Arduino Ide we need to write the code for the functioning of the robot and should be uploaded into the Arduino nano board and power should be supplied using the Mophie Juice Pack Powersation Pro.

after building the first prototype like mentioned above we can start upgrading the last prototype 
- first we need to upgrade the Design of the whole robot by redesigning the parts again so that it fits new parts in it i.e like battery pack etc and robot should be rebuilt .
- then we need to attach the Hc05 Bluetooth module to the arduino nano
- now we need to develop a simple app lusing MIT app inventor which gives input to the arduino module to which direction it shout move like left, right, forward, backward, a complete turn and other things if you want like u can even make it dance by using appropriate code.
- now we need to update the code of the arduino nano using Arduino Ide so that it responds to the appropriate commands given through the smartphone apk.
- now we need to connect the arduino nano to the  TP4056 1-cell Li-Ion Charging module which in turn is connected to the two Li-Po 18650 3.7v 2600mAh batteries connected in series and proably attach a switch in between to turn on while testing 
