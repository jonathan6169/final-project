int sensorValue ;
int sensorLow = 1023;
int sensorHigh = 0;
const int ledPin = 13;

void setup() {
  pinMode(ledPin, OUTPUT);
  while(millis() < 5000){
    sensorValue = analogRead(A0);
    if (sensorValue < sensorLow){
      sensorHigh = sensorValue
    }
    if (sensorValue > sensorLow){
      sensorLow = sensorValue
    }
  }
  
  // put your setup code here, to run once:

}

void loop() {
  sensorValue = analogRead(A0);
  int pitch = map(sensorValue, sensorLow, sensorHigh, 50, 4000);
  
  
  // put your main code here, to run repeatedly:

}
