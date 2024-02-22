INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-




*AIM*:  To interface a Analog  input (angular displacement sensor POT) and scale the values up on change in the input.


*COMPONENTS REQUIRED:*
1.	10 KΩPOT
2.	1 KΩ resistor 
3.	Arduino Uno 
4.	USB Interfacing cable 
5.	Connecting wires 
6.	LED of choice 
**


*THEORY*: 

*Analog signals:*

Analog signals – directly measurable quantities in terms of some other quantity.
Examples:
1. Thermometer – mercury height rises as temperature rises
2. Car Speedometer – Needle moves farther right as you accelerate
3. Stereo – Volume increases as you turn the knob
Reason for conversion of analog to digital quantity is that as the controller or any microprocessor works with digital signals in the form of 0 and 1s, in order to make the signal compatible  most of the analog signals are converted into its equivalent digital level signals using an analog to digital converter .
Quantizing - breaking down analog value is a set of finite states
Encoding - assigning a digital word or number to each state and matching it to the input signal
 There are two ways to best improve accuracy of A/D conversion:
Increasing the resolution which improves the accuracy in measuring the amplitude of the analog signal.
Increasing the sampling rate which increases the maximum frequency that can be measured.
General specifications of analog sensor
	1. Range
	2. Accuracy
	3.Linearity
	4.Compatiblity
	5. signal conversion capability

*Potentiometer*
A potentiometer, informally a pot, is a three-terminal resistor with a sliding or rotating contact that forms an adjustable voltage divider. If only two terminals are used, one end and the wiper, it acts as a variable resistor or rheostat.
Potentiometers are commonly used to control electrical devices such as volume controls on audio equipment. Potentiometers operated by a mechanism can be used as position transducers, for example, in a joystick. Potentiometers are rarely used to directly control significant power (more than a watt), since the power dissipated in the potentiometer would be comparable to the power in the controlled load
CIRCUIT DIAGRAM





![image](https://user-images.githubusercontent.com/36288975/163530788-eec3cdc3-95e8-4d2d-8349-6d0ea4c9439c.png)

**FIGURE -01
**

*PROCEDURE:*

1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select your board (If you the board is arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error , clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device 



*PROGRAM* 
 ~~~
int led =2;
int sensorpot;
void setup()
{
  pinMode(led, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  sensorpot = analogRead(A2);
 // Serial.print("data=");
  Serial.println(sensorpot);
  if(sensorpot>500)
  {
    digitalWrite(led,HIGH);
      delay(100);
    digitalWrite(led,LOW);
       delay(100);
  }
  else {
    digitalWrite(led,LOW);
      delay(100);
  }
}
~~~
![Screenshot 2024-02-22 111648](https://github.com/psomu31/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/145972430/05009e45-32a7-466b-a7da-1b9b3b14cfb4)


**
*Simulation output:* 
**
![Screenshot 2024-02-22 110959](https://github.com/psomu31/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/145972430/3c50980e-e783-4429-b786-9f256ce0495f)
![Screenshot 2024-02-15 110750](https://github.com/psomu31/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/145972430/0f7a75f8-a3d1-4761-b839-f151033066fb)


**RESULT: ** Arduino uno analog input functioning is learned and interfaced with digital input switch .INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-




*AIM*:  To interface a Analog  input (angular displacement sensor POT) and scale the values up on change in the input.


*COMPONENTS REQUIRED:*
1.	10 KΩPOT
2.	1 KΩ resistor 
3.	Arduino Uno 
4.	USB Interfacing cable 
5.	Connecting wires 
6.	LED of choice 
**


*THEORY*: 

*Analog signals:*

Analog signals – directly measurable quantities in terms of some other quantity.
Examples:
1. Thermometer – mercury height rises as temperature rises
2. Car Speedometer – Needle moves farther right as you accelerate
3. Stereo – Volume increases as you turn the knob
Reason for conversion of analog to digital quantity is that as the controller or any microprocessor works with digital signals in the form of 0 and 1s, in order to make the signal compatible  most of the analog signals are converted into its equivalent digital level signals using an analog to digital converter .
Quantizing - breaking down analog value is a set of finite states
Encoding - assigning a digital word or number to each state and matching it to the input signal
 There are two ways to best improve accuracy of A/D conversion:
Increasing the resolution which improves the accuracy in measuring the amplitude of the analog signal.
Increasing the sampling rate which increases the maximum frequency that can be measured.
General specifications of analog sensor
	1. Range
	2. Accuracy
	3.Linearity
	4.Compatiblity
	5. signal conversion capability

*Potentiometer*
A potentiometer, informally a pot, is a three-terminal resistor with a sliding or rotating contact that forms an adjustable voltage divider. If only two terminals are used, one end and the wiper, it acts as a variable resistor or rheostat.
Potentiometers are commonly used to control electrical devices such as volume controls on audio equipment. Potentiometers operated by a mechanism can be used as position transducers, for example, in a joystick. Potentiometers are rarely used to directly control significant power (more than a watt), since the power dissipated in the potentiometer would be comparable to the power in the controlled load
CIRCUIT DIAGRAM





![image](https://user-images.githubusercontent.com/36288975/163530788-eec3cdc3-95e8-4d2d-8349-6d0ea4c9439c.png)

**FIGURE -01
**

*PROCEDURE:*

1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select your board (If you the board is arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error , clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device 



*PROGRAM* 
 ~~~
int led =2;
int sensorpot;
void setup()
{
  pinMode(led, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  sensorpot = analogRead(A2);
 // Serial.print("data=");
  Serial.println(sensorpot);
  if(sensorpot>500)
  {
    digitalWrite(led,HIGH);
      delay(100);
    digitalWrite(led,LOW);
       delay(100);
  }
  else {
    digitalWrite(led,LOW);
      delay(100);
  }
}
~~~
![WhatsApp Image 2024-02-22 at 13 43 15_1d12877a](https://github.com/sanjaysivaramakrishnan/EXPERIMENT-NO--03-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/151629616/dfbf54be-31b5-419c-840d-04593a64ef56)


**
*Simulation output:* 
**
![Screenshot 2024-02-22 110959](https://github.com/psomu31/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/145972430/3c50980e-e783-4429-b786-9f256ce0495f)
![Screenshot 2024-02-15 110750](https://github.com/psomu31/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/145972430/0f7a75f8-a3d1-4761-b839-f151033066fb)


**RESULT: ** Arduino uno analog input functioning is learned and interfaced with digital input switch .
