# MQ135-sensor-working-code
Interfacing MQ135 with arduino basic code
#include <MQ135.h>

#include <MQ135.h>

#include "MQ135.h"
void setup (){
Serial.begin (9600);
}
void loop() {
MQ135 gasSensor = MQ135(A0); // Attach sensor to pin A0
float rzero = gasSensor.getRZero();
Serial.println (rzero-2100);
delay(1000);
}
