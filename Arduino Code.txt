#define BLYNK_TEMPLATE_ID "TMPL3KJ3t0jmE"
#define BLYNK_TEMPLATE_NAME "smart street"
#define BLYNK_AUTH_TOKEN "10nyR5uxereuBIXet5EhzYZG7qjPRed8"
#define BLYNK_PRINT Serial
#include <ESP8266WiFi.h>
#include <BlynkSimpleEsp8266.h>
char auth[] = BLYNK_AUTH_TOKEN;
char ssid[] = "redmi"; 
char pass[] = "12345678"; 
int ledpin = D0;
int ledpin1 = D1;
int ledpin2= D2;
BlynkTimer timer;
void setup()
{
Serial.begin(115200);
Blynk.begin(auth, ssid, pass); 
pinMode(ledpin,OUTPUT);
pinMode(ledpin1,OUTPUT);
pinMode(ledpin2,OUTPUT);
pinMode(D5,INPUT);
pinMode(D7,INPUT);
pinMode(D8,INPUT);
timer.setInterval(2500L, sendSensor);
}
void sendSensor(){
Blynk.virtualWrite(V4, D7);
Serial.println(D7);
if(digitalRead(D7)==HIGH){
// Blynk.email(“niralthiruvizha2024@gmail.com”, "Alert", "Light 1 Fault 
Detected!");
Blynk.logEvent("light_alert"," Light 1 Fault Detected!");
}
else if(digitalRead(D6)==HIGH){
// Blynk.email("niralthiruvizha2024@gmail.com", "Alert", " Light 2 Fault 
37
Detected!");
Blynk.logEvent("light_alert1"," Light 2 Fault Detected!");
}
else if(digitalRead(D5)==HIGH){
// Blynk.email("niralthiruvizha2024@gmail.com", "Alert", " Light 3 Fault 
Detected!");
Blynk.logEvent("light_alert2"," Light 3 Fault Detected!");
}
}
void loop()
{
Blynk.run();
timer.run();
}
BLYNK_WRITE(V0){
int value=param.asInt();
digitalWrite(ledpin,value);
}
BLYNK_WRITE(V1){
int value=param.asInt();
digitalWrite(ledpin1,value);
}
BLYNK_WRITE(V2){
int value=param.asInt();
digitalWrite(ledpin2,value);
}
