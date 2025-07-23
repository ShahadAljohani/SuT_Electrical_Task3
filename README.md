# SuT_Electrical_Task3
Task 3 - Week 3 (Summer Training)

-----------

## About this task
A latching power switch circuit with auto power off and on

----------

## Hardware configuration 

https://github.com/user-attachments/assets/989bb55e-7de4-4ace-89c4-d7773f2d5966

------------

## Implementation
```
const int Switch = 2, LED = 3;
int state = 0, LEDstate=0;

void setup()
{
  pinMode(Switch, INPUT);
  pinMode(LED, OUTPUT);
  Serial.begin(9600);
}
void loop()
{
  if (state == 0 && digitalRead(Switch) == HIGH) {
    state = 1;
    LEDstate=!LEDstate;
  }
  if (state == 1 && digitalRead(Switch) == LOW) {   
    state = 0;
  }
   digitalWrite(LED, LEDstate);
}
```
