# Encoder

```C++
#define HALL1 3
#define SPEED_1      5 
#define DIR_1        4
 
#define SPEED_2      6
#define DIR_2        7
 
volatile int count = 0;

void setup() {
 pinMode(HALL1, INPUT);
 Serial.begin(9600);
 attachInterrupt(digitalPinToInterrupt(HALL1), counter, CHANGE);
for (int i = 4; i<8; i++){
  pinMode(i, OUTPUT);
  }
}


void counter(){
  count++;
}

void loop() {
  Serial.println(count);
  digitalWrite(DIR_1, LOW);
  analogWrite(SPEED_1, 255);
}
```
