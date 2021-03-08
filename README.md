![thePlan_BH](https://user-images.githubusercontent.com/72640578/110393874-5b688600-8039-11eb-9da3-6a643a7000c4.jpg)
The original concept was very sweet: a small "Thinking of You" light for couples in long distance relationships (LDR). Intended to be small, the base would have a ribbon sensor used to slide/send your LDR partner a quick light "message" to let them them you're thinking about them. If they happened to see it when it "came in" on their end, they could then press a force-sensitive-resistor (FRS) to send some love back to let you know they got the message. Lit with a 10mm RGB led, the colors could blend from red to pink.

Whether complications with technology or the technologist, that design didn't work out as planned. 

So, plan B: make a single light interact (with the intention of developing it into a communicating light set.)
Wanting to add more layers to the communication, I decided to make the light flash three colors: Miss You Orange, Want You Pink, and Love You Red. This way there could be more layers to the silent communication of the light.
Using a single button, LDR 1 would press it once for Orange, twice for Pink and three times for Red.
The light would then turn on for LDR 2, rotating through all three colors three times (4.5 seconds), and would then stay on the color selected for another 4.5 seconds before blinking on off three times and then, ultimately, turning off again.

No matter how hard I looked, I could not for the life of me figure out how to blink an RGB led on and off. All tutorials showed only select pins turning off––but all three colors/pins are needed to create the color so turning off one would just change the color and not blink.
Secondarily, even after working for some time, suddenly "setColor" no longer worked. (I say suddenly because it worked, and then it didn't.)

Going forward, I would like to follow the above purpose of the "Thinking of You" lights with the added multi-light communicators. I like the dimension it adds while still remaining very simple. Perhaps there would be an added "response"/"I got you babe" button to send a got-your-message-and-ditto light...

Very frustrating but also very rewarding. I have not understood coding through this whole program but this project made it more fun :)


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

![thePlan_BH](https://user-images.githubusercontent.com/72640578/110393923-79ce8180-8039-11eb-8e27-572024162338.jpg)

![theSetup_BH](https://user-images.githubusercontent.com/72640578/110391721-e9427200-8035-11eb-83ad-252d5937f221.jpg)

https://youtu.be/FF4ADoFApoY // the light

https://youtu.be/kHPArCHbWNE // the light in an upside down candlestick holder

