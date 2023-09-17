# ROBOTICS_PROJECT_1
//Line follower robot code.

void setup() {
   
 pinMode(9,INPUT);    // Input pins.
 pinMode(10,INPUT);
 
 pinMode(2,OUTPUT);    // Output pins.
 pinMode(3,OUTPUT);
 pinMode(4,OUTPUT);
 pinMode(5,OUTPUT);
}

void loop() {

  int IR_R = digitalRead(9);
  int IR_L = digitalRead(10);

  if (( IR_R == 1 )&&( IR_L == 1))
  {
    digitalWrite(2,HIGH);
    digitalWrite(3,LOW); 
    digitalWrite(4,HIGH);
    digitalWrite(5,LOW);
  }

   else if (( IR_R == 1 )&&( IR_L == 0))
  {
    digitalWrite(2,LOW);
    digitalWrite(3,LOW); 
    digitalWrite(4,HIGH);
    digitalWrite(5,LOW);
  }

  else if (( IR_R == 0 )&&( IR_L == 1))
  {
    digitalWrite(2,HIGH);
    digitalWrite(3,LOW); 
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }

  else 
  {
    digitalWrite(2,LOW);
    digitalWrite(3,LOW); 
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
}
