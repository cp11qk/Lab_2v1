


//----------[Variables]----------
//
int led1 = 2; 
int led2 = 3;
int led3 = 4;
int buttonPin = 8;
int buttonInput = 0; 
//
int currentCase = 1;

void setup()
{
  pinMode(buttonPin, INPUT); // sets pinmodes
  pinMode(led3, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led1, OUTPUT);
}

void loop()
{
  //------[cases]------
  //
  switch (currentCase) {
  case 1:
    digitalWrite(led1, HIGH);
    break;
  case 2:
    digitalWrite(led2, HIGH);
    break;
  case 3:
    digitalWrite(led3, HIGH);
    break;
  }
  //
  buttonInput = digitalRead(buttonPin);
  //
  if(buttonInput == HIGH && currentCase != 3){   // if button is pressed, change case/led
    currentCase++;   
  }
  else if(buttonInput == HIGH && currentCase == 3){ // if currentCase is 3, revert back to 1
    currentCase = 1;
  }
}

















