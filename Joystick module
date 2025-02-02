#define vrx A0
#define vry A1
#define m1 2
#define m2 3
#define m3 4
#define m4 5
void setup()
{
  Serial.begin(9600);//inner screen
  Serial.print("welcome");
 pinMode(vrx , INPUT);

 pinMode(vry , INPUT);
 pinMode(m1 , OUTPUT); 
 pinMode(m2 , OUTPUT);
 
 pinMode(m3 , OUTPUT);
 pinMode(m4 , OUTPUT);
}

void loop()
{
 int xvalue = analogRead(vrx);
 int yvalue = analogRead(vry);
 int x = map (xvalue, 0, 1023, 0,100);
 int y = map (yvalue, 0, 1023, 0,100);
 Serial.println("X-axis: "+String(x));
 Serial.println("Y-axis: "+String(y));
 if ((x >=90)&&(y<=60)&&(y>=40))
 {
  Serial.println("Moving Backward");
  backward();
 }else if ((x <=10)&&(y<=60)&&(y>=40)){
   Serial.println("Moving Forward");
   forward();
 }else if ((y <=10)&&(x<=60)&&(x>=40)){
   Serial.println("Moving Right");
   right();
 }else if ((y >=90)&&(x<=60)&&(x>=40)){
   Serial.println("Moving Left");
   left();
 }else if ((y <=89)&&(y>=11)&&(x<=89)&&(x>=11)){
   Serial.println("Stopped");
   Stop();
 }else if ((x==100)&&(y==100)){
   Serial.println("Not Getting Values");
 }
delay(500);
}


void forward()
{
  digitalWrite(m1, HIGH);
  digitalWrite(m2, LOW);
  digitalWrite(m3, HIGH);
  digitalWrite(m4, LOW);
}
void backward()
{
  digitalWrite(m1, LOW);
  digitalWrite(m2, HIGH);
  digitalWrite(m3, LOW);
  digitalWrite(m4, HIGH);
}

void left()
{
  digitalWrite(m1, LOW);
  digitalWrite(m2, HIGH);
  digitalWrite(m3, HIGH);
  digitalWrite(m4, LOW);
}

void right()
{
  digitalWrite(m1, HIGH);
  digitalWrite(m2, LOW);
  digitalWrite(m3, LOW);
  digitalWrite(m4, HIGH);
}



void Stop()
{
  digitalWrite(m1, LOW);
  digitalWrite(m2, LOW);
  digitalWrite(m3, LOW);
  digitalWrite(m4, LOW);
}
