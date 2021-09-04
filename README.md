# ELEC.01.03.H-bridge-driver
Controlling 2 DC motor with an L293D(H bridge motor driver) and an Arduino. This is an implementation for two-wheel robot base.

The motors are programmed to simultaneously move clockwise for 2 seconds and then anticlockwise for another 2 seconds

There are 4 componants in this design (H-bridge l293, Arduino Uno R3, Breadboard, 2 DC Motors)

Result:
![Copy of Run and Control DC-Motor by using H-bridge Motor Driver  L293D  in Arduino](https://user-images.githubusercontent.com/85634568/132078105-0485c930-aa24-44bd-a8c3-2087879bdd4c.png)


code:
void setup()
{
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(11, OUTPUT);
  digitalWrite(13, HIGH);//set this pin to HIGH to enable motor driver
  
  
  pinMode(8, OUTPUT);
  pinMode(10, OUTPUT);
  pinMode(9, OUTPUT);
  digitalWrite(8, HIGH);//set this pin to HIGH to enable motor driver
  
}

void loop()
{
  digitalWrite(12, HIGH);
  digitalWrite(11, LOW);
  
  digitalWrite(10, HIGH);
  digitalWrite(9, LOW);
  //Use following block of code to run DC motor in anti clockwise
  //Use only if it is required
  delay(2000);
  
  digitalWrite(12, LOW);
  digitalWrite(11, HIGH);
  
  digitalWrite(10, LOW);
  digitalWrite(9, HIGH);
  
  delay(2000);
  
}
