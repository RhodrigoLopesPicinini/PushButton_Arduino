# PushButton_Arduino

void setup()
{
  pinMode(2, INPUT);
  pinMode(4, OUTPUT);
  pinMode(9, INPUT);
  pinMode(11, OUTPUT);
}

void loop()  {
  if (digitalRead(2) == HIGH) {
      digitalWrite(4, HIGH);
  }
  else {
    digitalWrite(4, LOW);
       }
  
  if (digitalRead(9) == HIGH) {
      digitalWrite(11, HIGH);
  
  }
  else {
    digitalWrite(11, LOW);
    
    if (digitalRead(12) == HIGH) {
        digitalWrite(13, HIGH);
        digitalWrite(11, HIGH);
        digitalWrite(4, HIGH);
    }
    else {
      digitalWrite(13, LOW);
      digitalWrite(11, LOW);
      digitalWrite(4, LOW);
    }
  
}
}
