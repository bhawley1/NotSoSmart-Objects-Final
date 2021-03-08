#include <RGBLed.h>
#include <analogWrite.h>
#define COMMON_ANODE

//  Sketch: Multiple states of the button
//
//  An  example of using a single button switch to set multiple states or conditions
//
//  state holds the current status.
//  0 = all off.
//  1 = Miss You
//  2 = Want You
//  3 = Love You
// Define the pins being used

const int buttonPin = A7; // the number of the pushbutton pin
const int redPin = A11;
const int greenPin = A10;
const int bluePin = A9;

int buttonState = 0;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(redPin, OUTPUT);
  pinMode(greenPin, OUTPUT);
  pinMode(bluePin, OUTPUT);

  Serial.begin(9600);
}
void loop() {
  buttonState = digitalRead(buttonPin);
  
  if (buttonState = HIGH); {
    for (int i = 0; i<3; i++)
    {
      setColor(255, 89, 0); // Miss You Orange
      delay(500);
      setColor(247, 5, 130); // Want You Pink
      delay(500);
      setColor(247, 5, 5); // Love You Red
      delay(500);
      }
      
      int j = 0; //create the variable that controls the while lop and set it to zero
      
      while (j<3) //begin the while loop and run as long as j is less than 2
      {
        setColor(255, 89, 0); // Miss You Orange
        delay(3000);
        }
        
        j++; //increase the value of j by 1 after each blink
        }
}



![theSetup_BH](https://user-images.githubusercontent.com/72640578/110391721-e9427200-8035-11eb-83ad-252d5937f221.jpg)

https://user-images.githubusercontent.com/72640578/110390998-db402180-8034-11eb-82a5-4e8b516fcb53.mov

