<h3 align="center">ARDUINO</h3>

### Basic
To learn about arduino basic click <a href="https://www.nexmaker.com/doc/5arduino/arduino_basic.html">here</a>

### Class Practice
<h2 align="center">LED control with switch</h2>
Controlling two LEDs with a switch using an Arduino is a common beginner project that demonstrates input and output interfacing. Below is a step-by-step process to achieve this:

Components Required:

- Arduino board
- Two LEDs (different colors)<br>
- Two 220-ohm resistors (or appropriate resistors for your LEDs)
- one 1040 kΩ Resistor
- Momentary push-button switch

Step 1: Circuit Connection

- Place your Arduino board on the breadboard.
- Connect the longer leg (anode) of the first LED to digital pin 2 on the Arduino. Use a 220-ohm resistor in series with this LED to limit the current.
- Connect the anode of the second LED to digital pin 3 on the Arduino, also with a 220-ohm resistor.
- Connect the shorter leg (cathode) of both LEDs to the Arduino's ground (GND) pin.
- Connect one terminal of the momentary push-button switch to digital pin 4 on the Arduino.
- Connect the other terminal of the push-button switch to the Arduino's ground (GND) pin.

Step 2: Write the arduino Code
~~~
    const int LED1=12;
const int LED2=13;
int val=0; 
void setup()
{ 
  pinMode(LED1, OUTPUT); 
  pinMode(LED2, OUTPUT); 
  pinMode(7, INPUT);     
}
void loop(){
val=digitalRead(7);
  if(val==HIGH)
{
    digitalWrite(LED1,HIGH);
    digitalWrite(LED2,LOW);
}
else
{ 
    digitalWrite(LED2,HIGH);
    digitalWrite(LED1,LOW);  
}
delay(1000);
}
~~~

Step 3: Upload the Code

- Open the Arduino IDE on your computer.
- Select the appropriate Arduino board and port from the "Tools" menu.
- Copy and paste the code into the Arduino IDE.
- Click the "Upload" button (right arrow) to upload the code to your Arduino board.

Step 4: Test the Circuit

After uploading the code, the LEDs will start in the OFF state. Press the push-button switch, and both LEDs should toggle between ON and OFF states with each press.
<br>

Simulation in Arduino simulation software.Here we use <a href="https://www.tinkercad.com/dashboard"> Tinkercad</a>
<br>
<img src="img/arduino/ar_simulation.png">
<style>
video-container {
            text-align: center;
        }
        video {
            max-width: 100%;
            max-height: 100%;
        }

</style>
Project video
<div id="video-container">
        <video controls>
            <source src="video/video_arduino/ar_s_video.mp4" type="video/mp4">
        </video>
    </div>

This project demonstrates the basic concept of digital input (reading the switch) and digital output (controlling the LEDs) using an Arduino.

<hr>

### Water Dispenser
<h2 align="center">WATER DISPENSER USING ARDUINO</h2>

<b>Project Overview</b> -<br> The Water Dispenser using Arduino is a smart and automated solution for dispensing water without physical contact. The system incorporates an Arduino UNO microcontroller, a single-channel relay module, an ultrasonic sensor, a mini-DC pump, pipes for water flow, jumper wires for connections, and power supply options such as 9v batteries, power bank, or a DC 9v power supply.
<br>
<br>
<b>Key Components</b> -
<br>
<br>
<b>Arduino UNO</b>: The brain of the system, responsible for processing data from the ultrasonic sensor and controlling the pump through the relay module.<br>

<b>Single-channel Relay Module</b>: This module acts as a switch to control the mini-DC pump. The Arduino triggers the relay to turn the pump on or off.<br>

<b>Ultrasonic Sensor</b>: Detects the presence of a user by sending and receiving ultrasonic waves. The Arduino calculates the distance based on the time taken for the waves to bounce back.<br>

<b>Mini-DC Pump</b>: Dispenses water when activated by the relay module. It ensures a controlled and precise flow.<br>

<b>Pipe</b>: Connects the water source to the pump and directs the water flow. It's a crucial component for the dispensing mechanism.<br>

<b>Jumper Wires</b>: Used for making electrical connections between components, linking the Arduino, relay module, ultrasonic sensor, and pump.<br>

<b>Power Supply Options</b>: The project can be powered using 9v batteries, a power bank, or a DC 9v power supply, providing flexibility and convenience.
<br>

<b>Working Principle</b> -<br>
The ultrasonic sensor continuously monitors the surroundings.
When a user approaches, the sensor detects the change in distance.
The Arduino processes this information and triggers the relay module to activate the pump.
The pump dispenses water through the connected pipe for a specified duration.
After dispensing, the system waits for the next user or enters a standby mode to conserve power.
<br>

<b>Applications</b> -<br> This Arduino-based water dispenser finds applications in various settings, including offices, public places, or homes, providing a touch-free and efficient way to access water.
<br>

<b>Components Photo</b> -
<br>
<br>
<img src="img/arduino/arduino_pic1.png">
<br>
<br>
<b>SKETCH DIAGRAM</b> -
<br>
<br>
<img src="img/arduino/arduino_pic2.png">
<br>
<br>
<b>Connection of all component</b> -
<br>
<br>
<img src="img/arduino/arduino_pic3.png">
<br>
<br>

<b>Arduino Code</b> -

~~~
/Water dispenser
#define trigger 5
#define echo 4
#define Relay 6
float time=0,distance=0;
void setup()
{ 
  Serial.begin(9600);
  pinMode(trigger,OUTPUT);
  pinMode(echo,INPUT);
  pinMode(Relay,OUTPUT);
  
  delay(2000);
}
void loop()
{
 measure_distance();
if(distance<5)
 {
  digitalWrite(Relay,LOW);
 }
 else
 {
  digitalWrite(Relay,HIGH);
 }
 
 delay(500);
}
void measure_distance()
{
  digitalWrite(trigger,LOW);
  delayMicroseconds(2);
  digitalWrite(trigger,HIGH);
  delayMicroseconds(10);
  digitalWrite(trigger,LOW);
  delayMicroseconds(2);
  time=pulsein(echo,HIGH);
  
  distance=time*200/20000; 
}
~~~

<b>Workflow</b> - 

Initialization:

- The Arduino initializes the necessary pin modes and begins serial communication.
The setup() function configures the pins for the ultrasonic sensor (trigger and echo) and the relay.

* Distance Measurement Loop (loop() function):

- The program continuously measures the distance using the measure_distance() function.

- It checks whether an object is within the specified distance (less than 5 units in this case).

Distance Measurement (measure_distance() function):

- The ultrasonic sensor sends a short pulse.

- It then measures the time taken for the pulse to bounce back (time it takes for the wave to return).

- The time is converted into distance using the speed of sound formula: distance = time * speed_of_sound / 2.
Note: Speed of sound is typically around 343 meters per second at room temperature.

Control of the Water Dispenser:

- If an object is detected within the specified range (less than 5 units), the relay turns off, assuming a cup or hand is present below the dispenser.
- If no object is detected within this range, the relay remains on, keeping the dispenser ready for use.

<b>Project Video</b> -
<div id="video-container"> 
    <video controls>
            <source src="img/arduino/water_dispenser.mp4" type="video/mp4">
        </video>
</div>

<b>Conclusion</b> -<br>
To sum up, the water dispenser using Arduino provides a hands-free and efficient solution for water dispensing. By combining an Arduino UNO, ultrasonic sensor, and mini-DC pump, the system responds to user proximity, offering a practical and hygienic approach. With versatile power options and simple components, it showcases the potential of DIY electronics in creating user-friendly, contactless systems with diverse applications.
<hr>


### IR Remote-Controlled LED Panel
<h2 align="center">IR Remote-Controlled LED Panel</h2>

<b>Project Overview</b> - The "IR Remote-Controlled LED Panel" project involves controlling LEDs using an IR remote. It's a simple demonstration of how IR signals can be used to trigger actions, in this case, turning LEDs on and off.
<br>

<b>Materials Needed</b>:
- Arduino board (e.g., Arduino Uno)
- IR Receiver module
- IR Remote control
- LEDs (4 or more)
- Breadboard and jumper wires
<br>
<img src="img/arduino/remotecontrollight_element.jpeg">
<br>
<br>

<b>Circuit Digram</b>
<img src="img/arduino/remotecontrollight_diagram.png">
<br>
<br>
<h2>Set Up</h2>
<br>

<b>Hardware Connection</b><br>

- Connect the IR Receiver module to the Arduino board.
- Connect LEDs to digital pins of the Arduino (LED1 to LED4 as mentioned in the code).
<img src="img/arduino/remotecontrollight_connection.jpeg">
<br>

<b>Software Setup</b><br>

- Install the IRremote library in the Arduino IDE (Tools > Manage Libraries).
- Use the provided code as the basis for your Arduino sketch.
<br>

<b>Code</b><br>

~~~
#include <IRremote.h>

const byte IR_RECEIVE_PIN = 2;

#define LED1 8
#define LED2 9
#define LED3 10
#define LED4 11

void setup()
{
   Serial.begin(115200);
   Serial.println("IR Receive test");
   IrReceiver.begin(IR_RECEIVE_PIN, ENABLE_LED_FEEDBACK);

   pinMode(LED1, OUTPUT);
   pinMode(LED2, OUTPUT);
   pinMode(LED3, OUTPUT);
   pinMode(LED4, OUTPUT);
}

void loop()
{
   if (IrReceiver.decode())
   {
      String ir_code = String(IrReceiver.decodedIRData.command, HEX);
      Serial.println(ir_code);

      if(ir_code == "c")
        digitalWrite(LED1, HIGH);
      else if(ir_code == "18")
        digitalWrite(LED1, LOW);
      if(ir_code == "5e")
        digitalWrite(LED2, HIGH);
      else if(ir_code == "8")
        digitalWrite(LED2, LOW);
      if(ir_code == "1c")
        digitalWrite(LED3, HIGH);
      else if(ir_code == "5a")
        digitalWrite(LED3, LOW);
      if(ir_code == "42")
        digitalWrite(LED4, HIGH);
      else if(ir_code == "52")
        digitalWrite(LED4, LOW);
      
      IrReceiver.resume();
   }
}
~~~

<b>Code Explanation</b><br>

- The code initializes the IR Receiver and sets up LEDs as outputs.
- It continuously checks for received IR signals using the IrReceiver.decode() function.
- When an IR signal is received, it decodes the signal and checks for specific codes (for the remote we use, it's IR code - 1 >'c', 2 >'18', 3 >'5e', 4 >'8', 5 >'1c', 6 >'5a', 7 >'42', 8 >'52'). (Remember that different remote has different IR code.)
- Based on the received code, it turns on or off specific LEDs connected to the Arduino.
<br>

<b>Testing</b><br>

- Upload the code to your Arduino board.
- Open the serial monitor (Tools > Serial Monitor) to see the decoded IR signal.
- Use the IR remote control to send signals corresponding to the codes mentioned in the code.
- Verify that pressing different buttons on the remote controls the LEDs as intended.
<br>

<b>Testing Video</b>
<div id="video-container"> 
    <video controls>
            <source src="img/arduino/remotecontrollight_video.mp4" type="video/mp4">
        </video>
</div>
<br>

<b>Conclusion</b>- The "IR Remote-Controlled LED Panel" project demonstrates how to use an IR remote to control LEDs connected to an Arduino. It showcases the functionality of IR receivers and how they can be integrated into projects for remote control applications. With modifications, it can be expanded to control more devices or perform diverse actions based on different IR signals received.
<hr>