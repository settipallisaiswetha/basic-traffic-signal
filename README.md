# basic-traffic-signal
# code
const int GREENLED = 13;
const int YELLOWLED = 12;
const int REDLED = 11;
const int buttonPin = 7;

int buttonState = 0;

void setup() {
  pinMode(GREENLED, OUTPUT);
  pinMode(YELLOWLED, OUTPUT);
  pinMode(REDLED, OUTPUT);
  
  pinMode(buttonPin, INPUT_PULLUP);
}

void loop() {
  buttonState = digitalRead(buttonPin);

  if (buttonState == LOW) {
    pedestriansCrossing();
  } else {
    digitalWrite(REDLED, HIGH);
    delay(5000); // Red for 5 seconds
    digitalWrite(REDLED, LOW); 
  digitalWrite(REDLED, HIGH);
  delay(7000); // Red for 7 seconds
  digitalWrite(REDLED, LOW);
    
   digitalWrite(YELLOWLED, HIGH);
    delay(3000); // Yellow for 3 seconds
    digitalWrite(YELLOWLED, LOW);
    digitalWrite(REDLED, HIGH);
  delay(7000); // Red for 7 seconds
  digitalWrite(REDLED, LOW);
    
   digitalWrite(GREENLED, HIGH);    
    delay(5000); // Green for 5 seconds
    digitalWrite(GREENLED, LOW);    
  digitalWrite(REDLED, HIGH);
  delay(7000); // Red for 7 seconds
  digitalWrite(REDLED, LOW);

    
   digitalWrite(YELLOWLED, HIGH);
    delay(3000); // Yellow for 3 seconds
  digitalWrite(YELLOWLED, LOW);
     digitalWrite(REDLED, HIGH);
  delay(7000); // Red for 7 seconds
  digitalWrite(REDLED, LOW);
    
  }
}

void pedestriansCrossing() {
  // RED light for pedestrians to cross
  digitalWrite(REDLED, HIGH);
  delay(7000); // Red for 7 seconds
  digitalWrite(REDLED, LOW);
}



   The goal here is to put together a basic traffic light with a pedestrian crossing feature, kinda like the ones we see on the streets, but way smaller and cooler!

Stuff You'll Need:
1. Arduino Uno - It's like the boss of this whole operation, running the show for the LEDs and button.
2. Red, Yellow, and Green LEDs - These little guys will be our traffic lights, lighting up to tell cars and peeps when to go, slow down, or stop.
3. Some 220Ω resistors - These are like the bouncers for the LEDs, making sure they don't get too much current and burn out while they're working hard.
4. A push button - This is what the pedestrians will smack to tell the light they want to cross.
5. A 10kΩ resistor - This one's like a sidekick to the button, helping it do its job without messing up the circuit.
6. Breadboard and wires - Think of this as the playground where all the parts hang out and connect without the mess of soldering.

So, how does this bad boy work?

In the Normal Mode:
- The Arduino chills with the Green LED on, giving the thumbs up for cars to go ahead.
- After a bit, the Green LED goes off and the Yellow one comes on, which is basically the universe saying, "Hey, cars, the light's gonna change, so get ready."
- Then, the Yellow LED goes off, and the Red one starts blinking its stern, red eye, telling cars, "Nope, stop right there!"
- This whole cycle keeps repeating, just like the lights we all know and sometimes love.

But wait, there's more!
Pedestrian Crossing Mode:
- When a pedestrian hits the button, the Arduino gets the message.
- The system goes, "Oh, hold up!" and stops the car-focused cycle.
- The Red LED lights up, giving cars the universal signal to stop.
- If you've got a special pedestrian Green LED, it'll come on after cars are at a full stop, which means "Walkies time!" for the people crossing the street.
- Once the designated crossing time is up, the system goes back to its car-loving cycle, starting with the Green LED for vehicles.

So, that's the gist of it. It's like playing with a mini traffic jam without the actual jam part.ds





