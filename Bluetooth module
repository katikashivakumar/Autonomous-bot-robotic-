#include<SoftwareSerial.h>
SoftwareSerial bt(8,9);//(tx,rx)
#define m1 2
#define m2 3
#define m3 4
#define m4 5


void setup()
{
  Serial.begin(9600);//inner screen
  bt.begin(9600);//starting bluetooth module
 pinMode(m1 , OUTPUT);
 pinMode(m2 , OUTPUT);
 pinMode(m3 , OUTPUT);
 pinMode(m4 , OUTPUT);
}

void loop()
{
 
 if (bt.available()>0)//if data from the bluetooth
 {
  char data = bt.read();// read the data
  Serial.println(data);//print on inner screen
  if (data == '1'){
    bt.println("forward");//for inner screen
    forward();
  }if(data == '2'){
    backward();
  }if (data=='3'){
    left();
  }if (data=='4'){
    right();
  }if (data=='5'){
Stop();
  }
 }
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
