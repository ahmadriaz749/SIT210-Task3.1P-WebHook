# SIT210-Task3.1P-WebHook


int led1 = D7; 

int photoresistor = A0;
int analogValue;


void setup() {



  pinMode(led1, OUTPUT);
  pinMode(photoresistor, INPUT);

}


void loop() {
 
analogValue = analogRead(photoresistor);
String light = String(analogValue);
Particle.publish("temp", light, PRIVATE);

delay(30000);

 
}
