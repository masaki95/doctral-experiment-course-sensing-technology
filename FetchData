#include <math.h>
const int speakerPIN = 3;

void setup() {
 Serial.begin(9600);
 pinMode(speakerPIN, OUTPUT);
 TCCR2A = _BV(COM2B1) | _BV(WGM21) | _BV(WGM20);
 TCCR2B = _BV(CS20);
}

void loop() {
  int sensorValue = analogRead(A0);
  Serial.println(sensorValue);
  delay(10); 
}
