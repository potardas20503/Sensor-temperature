int dt,temp;
void setup()
{
  pinMode(A0,INPUT);
  Serial.begin(9600);
  
  pinMode(2,OUTPUT);
  
}

void loop()
{
  
  dt = analogRead(A0);
  temp = map( dt, 20, 358, -40, 125);
  Serial.print("temp = ");
  Serial.println(temp);
  delay(1000); 
  
  if(temp < 40){
  digitalWrite(2,LOW);
  }else{
    digitalWrite(2,HIGH);
   }
 
}
