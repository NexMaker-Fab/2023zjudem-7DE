### IOT Cloud setup
Get NodeMcu information and then control NodeMcu with <a href="https://io.adafruit.com/">Adafruit IO</a>

Step 1: Adafruit IO Setup
  - Create an account on <a href="https://io.adafruit.com/">Adafruit IO</a>
  - From IO click feed click New feed
<br>

<img src="img/iot/iot1.png">
<img src="img/iot/iot2.png">
<br>
<br>

- Set the name and click create
<br>

<img src="img/iot/iot3.png">
<br>
<br>

- Now go to dashboard and click New Dashboard and set DashBoard name and create
<br>

<img src="img/iot/iot4.png">
<img src="img/iot/iot5.png">
<br>
<br>

- Now Click on the created Dashboard > click on setting icon > Click creat new block
<br>

<img src="img/iot/iot6.png">
<img src="img/iot/iot7.png">
<img src="img/iot/iot8.png">
<br>
<br>

- Now select the block (ON/OFF switch for our project) and click create
<br>

<img src="img/iot/iot9.png">
<br>
<br>

- Now select the created feed and click Next step and inpu the button on text and button off text.
<br>

<img src="img/iot/iot10.png"> 
<img src="img/iot/iot11.png">
<br>
<br>

- Now after turn on and turn off the switch we can see value for created feed.
<br>

<img src="img/iot/iot12.png">

### Arduino IDE setup

Step  2 :Arduino IDE setup
- Connect all hardware
<br>

<img src="img/iot/iotarduinosetup.jpeg">
<br>
<br>

- Now add the additional board manager URL(http://arduino.esp8266.com/stable/package_esp8266com_index.json)
<br>

<img src="img/iot/arduinoidepre.png">
<br>
<br>

- Open Arduino IDE and write the bellow code

~~~
    #include <ESP8266WiFi.h>
#include "AdafruitIO_WiFi.h"

#define WIFI_SSID     "YOUR WIFI_SSID"
#define WIFI_PASS     "WIFI_PASSWORD"
#define IO_USERNAME   "IO_USERNAME"
#define IO_KEY        " Your IO_KEY"


const int ledPin = D1; // Assuming the LED is connected to GPIO pin D1 (NodeMCU)


AdafruitIO_WiFi io(IO_USERNAME, IO_KEY, WIFI_SSID, WIFI_PASS);


AdafruitIO_Feed *LedFeed = io.feed("LED");

void setup() {
  Serial.begin(115200);
  pinMode(ledPin, OUTPUT);

  while (!Serial) {
    delay(100); // Wait for Serial to be available - necessary for some boards
  }
  
  Serial.println("Booting...");

  //*********************WiFi connection and Adafruit IO status

  Serial.print("Connecting to Wi-Fi");
  io.connect();


  while (io.status() < AIO_CONNECTED) {
    Serial.print(".");
    delay(500);
  }

  Serial.println();
  Serial.println("Connected to Adafruit IO!");


  LedFeed->onMessage(handleLedMessage);
  LedFeed->get();
}

void handleLedMessage(AdafruitIO_Data *data) {
  Serial.print("Received LED Data: ");
  int value = data->toInt();
  Serial.println(value);

  //2201cdrck
  if (value == 1) {
    digitalWrite(ledPin, HIGH); // Turn on the LED
    Serial.println("LED turned ON");
  } else if (value == 0) {
    digitalWrite(ledPin, LOW); // Turn off the LED
    Serial.println("LED turned OFF");
  }
}

void loop() {
  io.run();

}

~~~

- Define wifi SSID and Password and IO_USERNAME and IO_KEY
<br>

<img src="img/iot/iotarduinosetup1.png">
<br>
<br>

- For IO_USERNAME and IO_KEY go to Adafruit created feed and click the key icon.
<br>

<img src="img/iot/iot16.png">
<img src="img/iot/iot17.png">
<br>
<br>

- Install needed library esp8266 and Adafruit IO Arduino
<br>

<img src="img/iot/iot_esp8266.png">
<img src="img/iot/iot_adafruit.png">
<br>
<br>

- Now if the NodeMcu is not connected, connect the hardware with USB cable into your computer and go to tools > Boards > esp8266 > NodeMcu 1.0 (ESP 12E Module)
<br>

<img src="img/iot/select nodemcu.png">
<br>
<br>

- Now upload the code and make sure the wifi is connected on serial monitor
<br>

<img src="img/iot/iot_code_upload.png">
<br>
<br>

- GO back to Adafruit created Dashboard and turn on/ turn off the switch to control the LED connected with NodeMcu,
<br>

<video align="centre" width="100%" height="100%" controls muted>
  <source src="img/iot/iotarduinosetup_video.mp4" type="video/mp4">
</video>
