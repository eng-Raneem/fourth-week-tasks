# fourth-week-tasks
This repository includes the fourth week tasks
**Analog sensor **: I used temperature sensor (TMP36) as an analog sensor with a LCD screen to display the temperature The followin code was used to run the circuit:

// include the library code for LCD display: #include <LiquidCrystal.h>

// initialize the library with the numbers of the interface pins LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

// Defining pin #define temp A5 #define led 13

void setup() { // set up the LCD's number of columns and rows: lcd.begin(16, 2); pinMode(led, OUTPUT); pinMode(temp, INPUT); Serial.begin(9600); lcd.clear(); lcd.print("Temperature: "); } //Global Variable float pre_temp = 0; void loop() { float temperature = 0; temperature = (analogRead(temp) * 0.48828125) - 49.95; if(pre_temp != temperature) { lcd.setCursor(0,1); lcd.print(" "); } lcd.setCursor(0,1); lcd.print(temperature); lcd.print(" C"); pre_temp = temperature; }

you can also try the code by your own by visiting the following link : https://www.tinkercad.com/things/ajYv5SWOn9q-temperature-sensor/editel

**Digital sensor**: I used PIR (motion sensor) to turn on\off LED and a slide sensor to turn the LED on\off too in another connection You can also see the connections by visiting the following link: https://www.tinkercad.com/things/ifLI8voYBvy-digital-sensors/editel
