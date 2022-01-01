---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

# <u><b>Kerala IoT Challenge</b></u>
<blockquote>
  <p><strong>Foxlab Makerspace</strong> in association with <strong>GTech - Group of Technology Companies</strong> in Kerala is launching our prestigious program  <strong>“Kerala&nbsp;IoT Challenge 2021”</strong>,  with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. <strong>Kerala IoT Challenge</strong> is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.</p>
</blockquote>

# <u><b>About Me</b></u>
<blockquote>
Hi, I am  MOHAMED NIHAJ K. I am a Final year Computer engineering student  @ <a href="http://ssmpoly.ac.in/" target="_blank">SSM&nbsp; POLYTECHNIC &nbsp; COLLEGE&nbsp; TIRUR</a>Love to learn new things and I like to be updated with development in the Tech Industry. I am Fascinated  about Tech related stuff.  
</blockquote>
____

# <u><b>LEVEL - I</b></u>

# <u><b>Experiments</b></u>

## Exp 1 : Hello World LED Blinking

### Hardware Needed:
   * Arduino Uno Board x1
   * USB Cable x1
   * LED (Any Color) x1
   * 220 OHM Resistor X1 
   * Breadboard
   * Jumper Wires (Male to Male ) x2
### Image
[<img align="left" alt=""  src="./images/exp1.jpeg" />]
### Code
    int ledPin = 10; // define digital pin 10.
    void setup()
    {
     pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
    }
    void loop()
    {
     digitalWrite(ledPin, HIGH); // set the LED on.
     delay(1000); // wait for a second.
     digitalWrite(ledPin, LOW); // set the LED off.
     delay(1000); // wait for a second
    }


___


## Exp 2 : Traffic Light

### Hardware required
  * Arduino board x1
  * USB cable x1
  * Red M5 LED x1
  * Yellow M5 LED x1
  * Green M5 LED x1
  * 220Ω resistor x3
  * Breadboard x1
  * Breadboard jumper wires as needed
### Image
[<img align="left" alt=""  src="./images/exp2.jpeg" />]
### Code
    int red =10; // initialize digital pin 8.
    int yellow =7; // initialize digital pin 7.
    int green =4; // initialize digital pin 4.
    void setup()
    {
      pinMode(red, OUTPUT);// set red LED pin as “output”
      pinMode(yellow, OUTPUT); // set yellow LED pin as  “output”
      pinMode(green, OUTPUT); // set green LED pin as “output”
    }
    void loop()
    {
      digitalWrite(green, HIGH);// turn on green LED
      delay(5000);// wait 5 seconds
      digitalWrite(green, LOW); // turn off green LED
      for(int i=0;i<3;i++)// blinks for 3 times
      {
       delay(500);// wait 0.5 second
       digitalWrite(yellow, HIGH);// turn on yellow LED
       delay(500);// wait 0.5 second
       digitalWrite(yellow, LOW);// turn off yellow LED
      } 
      delay(500);// wait 0.5 second
      digitalWrite(red, HIGH);// turn on red LED
      delay(5000);// wait 5 seconds
      digitalWrite(red, LOW);// turn off red LED
    }


___

## Exp 3 : LED Chasing Effect

### Hardware required
  * LED x6
  * Arduino board x1
  * 220Ω resistor x6
  * Breadboard x1
  * USB cable x1
  * Breadboard wire x13
### Image
[<img align="left" alt=""  src="./images/exp3.jpeg" />]
### Code
    int first= 2;  // the I/O pin for the first LED
    int last= 6;   // number of LEDs
    void setup(){
     for (int i = start; i < first + last; i ++){
      pinMode(i, OUTPUT);   // set I/O pins as output
     }
    }
    void loop(){
     for (int i = BASE; i < start +; i ++){
      digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
      delay(200);        // delay
    }
     for (int i = BASE; i < BASE + NUM; i ++){
      digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
      delay(200);        // delay
     }  
    }


____

## Exp 4 : Button Controlled LED

### Hardware required
* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1
### Image
[<img align="left" alt=""  src="./images/exp4.jpeg" />]
### Code
    int ledpin=11;// initialize pin 11
    int inpin=3;// initialize pin 3
    int val;// define val
    void setup()
    {
    pinMode(ledpin,OUTPUT);// set LED pin as “output”
    pinMode(inpin,INPUT);// set button pin as “input”
    }
    void loop()
    {
    val=digitalRead(inpin);// read the level value of pin 3 and assign if to val
    if(val==LOW)// check if the button is pressed, if yes, turn on the LED
    { digitalWrite(ledpin,LOW);}
    else
    { digitalWrite(ledpin,HIGH);}
    }

____

## Exp 5 : Buzzer

### Hardware required
* Arduino Uno
* Buzzer x1
* Breadboard x1
* Breadboard Jumper Wire x2
* USB cable x1
### Image
[<img align="left" alt=""  src="./images/exp5.jpeg" />]
### Code
    int buzzer=8;// initialize digital IO pin that controls the buzzer
    void setup() 
    { 
      pinMode(buzzer,OUTPUT);// set pin mode as “output”
    } 
    void loop() 
    {
    digitalWrite(buzzer, HIGH); // produce sound
    }

____

## Exp 6 : RGB LED

### Hardware required
* Arduino Uno
* USB Cable x1
* RGB LED x1
* Resistor x3
* Breadboard jumper wire x5

### Code
    int redpin = 11; //select the pin for the red LED
    int bluepin =10; // select the pin for the blue LED
    int greenpin =9;// select the pin for the green LED
    int val;
    void setup() {
      pinMode(redpin, OUTPUT);
      pinMode(bluepin, OUTPUT);
      pinMode(greenpin, OUTPUT);
      Serial.begin(9600);
    }
    void loop() 
    {
    for(val=255; val>0; val--)
      {
      analogWrite(11, val);
      analogWrite(10, 255-val);
      analogWrite(9, 128-val);
      delay(1); 
      }
    for(val=0; val<255; val++)
      {
      analogWrite(11, val);
      analogWrite(10, 255-val);
      analogWrite(9, 128-val);
      delay(1); 
      }
    Serial.println(val, DEC);
    }

____

## Exp 7 : LDR Light Sensor
### Image
[<img align="left" alt=""  src="./images/exp7.jpeg" />]
### Hardware required
* Arduino Uno Board
* Photo Resistorx1
* Red M5 LED x1
* 10KΩ Resistor x1
* 220Ω Resistor x1
* Breadboard x1
* Breadboard Jumper Wire x5
* USB cable x1

### Code
    void setup() {
      pinMode(8,INPUT);
      pinMode(9,OUTPUT);
      Serial.begin(9600); //initialise serial monitor
    }

    void loop() {
      int temp=digitalRead(8);       //assign value of LDR sensor to a temporary variable
      Serial.println("Intensity="); //print on serial monitor using ""
      Serial.println(temp);         //display output on serial monitor
      delay(300);
      if(temp==HIGH)               //HIGH means,light got blocked
      digitalWrite(9,HIGH);        //if light is not present,LED on
      else
      digitalWrite(9,LOW);         //if light is present,LED off
    }



