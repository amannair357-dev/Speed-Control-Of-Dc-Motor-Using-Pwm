# Speed-Control-Of-Dc-Motor-Using-Pwm
Speed Control Of Dc Motor Using Pwm

## Program
~~~C++
int MPin = 9;   //motor pin
int Analog = A0;  // Analog Input
int Ainp = 0; // Read analog input, initialized to zero  
  
void setup()
{
  
  Serial.begin(9600);
  pinMode(MPin, OUTPUT);
  pinMode(Analog, INPUT);
}

void loop()
{

Ainp = analogRead(A0);

int Speed = map(Ainp, 0, 1024, 0, 255);
delay(100);
Serial.println(Speed);
analogWrite(MPin, Speed);  

}
~~~

## Output

<img width="1171" height="718" alt="exp5ior" src="https://github.com/user-attachments/assets/5da83026-e106-4d4e-94af-fbbb254d4975" />

## Result

Thus, the Speed Control Of Dc Motor Using Pwm is created and verified.
