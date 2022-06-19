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
- now we need to connect the arduino nano to the  TP4056 1-cell Li-Ion Charging module which in turn is connected to the two Li-Po 18650 3.7v 2600mAh batteries connected in series and probably attach a switch in between to turn on while testing 

# [Human Detection Robot](https://www.electronicshub.org/human-detection-robot/)
## Problem Statement:-
Designing a human detection robot which can be used for the rescue operations for detecting the Human Beings under the debris caused by the Natural calamaties like Earthquakes, Tsunamis, Floods etc. 
## Ideation and Planning:-
- PC-> RF transmitter & receiver-> AT89s51  microcontroller -> PIR sensor-> motor driver IC -> Motors

| Part of the Pipeline | Feasibility | Advantages | Disadvantages |
| :---: | :---: | :---: | :---: |
| PC | easy to transmit information from the PC using the Hyper terminal | it becomes easy to transfer the information from PC instead of using any other ways to give the input | logic levels of PC are ± 3v to ± 15V, while the logic levels of RF module is compatible with TTL which is disadvantageous.In order to convert this voltage we use another IC called MAX 232 |
| RF transmitter & receiver | easy to use and affordable | tranfers signals to longer distances of range 20m - 200m faster | data is only trasmitted at certain frequency and the uncontrolled radiation of RF methods can cause adverse affects to little birds and pre-adolescent children |
| AT89s51  microcontroller | Hard for the users who haven't worked with the Microcontroller prior to the project | easily programmable for the people who have experience in programming in C language | Hard for the new users of the Microcontroller and who don't have the Knowledge of the C Programming|
|PIR sensor| easily used and cheaper in costs | easily available and can detect the infra red radiations of very low wave length | even though the range of the PIR sensor is 10 m it is still less in some of the cases |
|motor driver IC| easy to use the L293D IC motor driver | can be useful to drive the motor and also eliminates back EMF generated and can take input voltage of range 2.4v to 36v| they become very hot when subjected to electric current more than 1A and can be damaged because of it |
|Motors| easy to connect and work with | can achieve high speeds and can run at different voltages | cannot achieve angular motion and speed cannot be precisely controlled |

## Choosing a new pipeline:-
- in this project uprading the projects and adding new components to the robot can make the project expensive.
- PC-> camera -> video reciever and transmitter ->  RF transmitter & receiver-> arduino microcontroller -> PIR sensor-> motor driver IC -> Motors

| new parts of the pipeline | Feasibility | Advantages | Disadvantages |
| :---: | :---: | :---: | :---: |
| video reciever and transmitter | feasible since it can be used to observe the areas affected due to natural disasters for human beings | advantageous for detecting the trace of Human beings and the route of the robot more accurately and safely| the cost of the video trasmitter and the reciever is quite high as the trasmission range we require is somewhat more than 20m |
| arduino microcontroller | hard to use for the beginners | instead of using many components like DB9 connector, MAX232 IC we can directly use a Arduino microcontroller like nano or uno connected to PC and RF Transmitter cause it can give out signals in TTL range input can be given using the serial monitor in Arduino IDE and a Arduino nano 33 BLE in receiver module can be used to get the informations like temp etc | the robot becomes more expensive when compared without any upgrades|

## Prototyping phase:-
- first of all the prototype will be developed using PC, RF transmitter, MAX232IC, DB9 connector as parts of the Transmitter section and AT89c51microcontroller, L293D motor driver IC, RF receiver, motors of the robot, PIR sensor as parts of the Receiver section as per the circutary given below.
### Transmitter Circuit:-
![Human-Detection-Robot-Circuit-Diagram-Transmitter-Section](https://user-images.githubusercontent.com/107262758/174491790-cf3ae17d-8527-47a3-b3ad-cf9414044683.jpg)
### Receiver Circuit:-
![Human-Detection-Robot-Circuit-Diagram-Receiver-Section](https://user-images.githubusercontent.com/107262758/174491796-fa7f585c-b0d7-4534-b75f-43bf561bb2cb.jpg)

- after testing the circuitary based on these we start ugrading our robot as per mentioned changes 
