# 15-de-febrero
Encendido y apagado de dos LEDs diferentes usando estructuras repetitivas y entrada al monitor serial

int led1=3;
int led2=4;
int t1;
int t2;

void setup() {
 Serial.begin(9600);
 Serial.println("Cuantas veces led Azul?");
 while(Serial.available() == 0){
 }
 t1=Serial.parseInt();
 pinMode(led1, OUTPUT);
 Serial.println("Cuantas veces led Rojo?");
 while(Serial.available()==0){
 }
 t2=Serial.parseInt();
 pinMode(led2, OUTPUT);
 }

void loop() {
  for (int i = 0; i < t1; i++){
    digitalWrite(led1, HIGH);
    delay(500);
    digitalWrite(led1, LOW);
    delay(200);
  }
  for (int i = 0; i < t2; i++){
    digitalWrite(led2, HIGH);
    delay(500);
    digitalWrite(led2, LOW);
    delay(200);
  }
}
