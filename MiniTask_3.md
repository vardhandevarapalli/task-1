# [Arduino Nano Quadruped Robot](https://www.instructables.com/Arduino-Nano-Quadruped-Robot/)
## Troubleshooting:-
- The sequence of the working of the robot is given below
- Power Supply-> Smartphone app ->Bluetooth Transreciver-> Microcontroller-> Arduino Expansion Shield-> Servo Motors
- lets start testing the whole project for errors.
- the order of testing error is according to the above mentioned sequence of working.
- first test if the power supply is good and then check if the smartphone apps code have any problem even a small error or bug in the code can cause the project to not work.
- then check if the bluetooth reciever is working well then microcontroller, then arduino exansion shield then the motors.
### Testing the Power Supply:-
- If none of the modules of the robot get the power supply then the problelm would be in the Power supply. 
- either the batteries are not charged or some other problem first try charging the batteries if the robot still not working then
- Check if any of the two Li-Po 18650 3.7v 2600mAh batteries connected in series are damaged or bulged , if damaged try using a batteries in place of them and test it.
- If not check if the two batteries are connected in series and the batteries are connected properly to the TP4056 1-cell Li-Ion Charging module.
- and check if the TP4056 1-cell Li-Ion Charging module is too hot and if it is there might be a chance that the charging module is damaged so try changing it to new one.
- by now the power supply might be  restored, its highly unlikely that all the modules not getting the powersupply even though the power supply is fine check if any one of the module is getting the power if yes then power supply is fine now move on to the next module (we can check the app at last) which is BLuetooth transreceiver.
### Testing the Smartphone app:-
- As i mentioned in the previous task we can create an app using the MIT app inventor. 
- so now check the code of the app and check if the proper word is transferred for the proper command like

| function | word |
| :---: |:---:|
| forward | f |
| backward | b |
| left | l |
| right | r |
- try to debug the code and check if you can find any errors if found again repeat the process again
- if not try to press forward and backward buttons in the smartphone app and see if it displays ;f' and 'b' in the serial monitor in the Arduino IDE software in the PC if not try checking the Bluetooth module
### Testing the Bluetooth:- 
- before attempting the last step of the last test try to upload the below mentioned code in the arduino nano. 

```
char Incoming_value = 0;                //Variable for storing Incoming_value
void setup() 
{
  Serial.begin(9600);         //Sets the data rate in bits per second (baud) for serial data transmission
}
void loop()
{
  if(Serial.available() > 0)  
  {
    Incoming_value = Serial.read();      //Read the incoming data and store it into variable Incoming_value
    Serial.print(Incoming_value);        //Print Value of Incoming_value in Serial monitor
    Serial.print("\n");        //New line 
  }                            
} 
```
- if you can see the same alphabets mentioned above for the commands that you have given then your bluetooth module and your app both are fine.
- if not still there is one step left for checking the bluetooth module.

- So , Your Input power to the Bluetooth is not sufficient for it to Work properly. Power the Arduino using a Power bank to get it working on the bot or Follow the Hack Below.

- Remove Vcc of Bluetooth Module and Connect it to Pin 2 of Arduino and Add the below lines to the Code.

- Add the Follow lines to void setup() function of the code mentioned above.

```
void setup(){
.
.
pinMode(2, OUTPUT);           // Add these two lines at the end of the function.
digitalWrite(2, HIGH);
}

```
here it tries to provide 5v to the bluetooth module which was initially provided with 3.3V.
- check if the connections are proper or any wires are shorted, if the Module is hot and its not yet working then change the module.
### testing Microcontroller & Arduino Expansion Shield & Servo Motors:-
- generally its so rare to get the arduino board damaged cause it already has many inbuit mechanisms to stop the board from damage.
- check if the arduino boards IC is hot then you cant even upload the code so you have to replace the arduino board with the new arduino nano board.
- if the arduino board is good then check for any shorted pins in the expansion shield.
- if its fine now follow the below steps.
- check if any pins are shorted in both the arduino nano and its expansion shield.
- now try checking if all the servos are working with the given code below.

```
#include <Servo.h>
Servo hip1;
Servo knee1;
Servo hip2;
Servo knee2;
Servo hip3;
Servo knee3;
Servo hip4;
Servo knee4;
void setup()
{
  hip1.attach(0);
  hip1.write(90);
  knee1.attach(1);
  knee1.write(90);
  hip2.attach(2);
  hip2.write(90);
  knee2.attach(3);
  knee2.write(90);
  hip3.attach(4);
  hip3.write(90);
  knee3.attach(5);
  knee3.write(90);
  hip4.attach(6);
  hip4.write(90);
  knee4.attach(7);
  knee4.write(90);
}
void check()
{
    hip1.write(180);
    hip2.write(180);
    hip3.write(180);
    hip4.write(180);
    delay(1000);
    knee1.write(180);
    knee2.write(180);
    knee3.write(180);
    knee4.write(180);
}
void loop()
{
    check();
}

```

- if any of the servos are not working try checking their wires for any loose connections if and the pin connections if all are fine then check the output pins of the expansion shield.
- if it still doesnt work then change the motor.
## conclusion:-
- by following these steps u can find the error in any one of the steps so in similar way you can debug mostof the projects.
- by the end of the tutorial we would have completed the debugging and our robot would finally be working.
