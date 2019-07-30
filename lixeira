#include <Servo.h>
#include <LiquidCrystal.h>


LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

//variavies sensor 1
int SensorSaida1 = 7; 
int SensorEntrada1 = 6;

float tempo1;
float distancia1;

//variavies sensor 2
int SensorSaida2 = 9;
int SensorEntrada2 = 8;

float tempo2;
float distancia2;

Servo servo_13;

void setup() {

    lcd.begin(16, 2); 
    Serial.begin(9600);
      
    lcd.setCursor(0, 0);
    lcd.print("    LIXEIRA ");
    lcd.setCursor(0, 1);
    lcd.print("  INTELIGENTE ");
    delay(5000);
      
    servo_13.attach(13);
    
  
    
    pinMode(SensorSaida1, OUTPUT);
    digitalWrite(SensorSaida1, LOW);
    delayMicroseconds(500);
    
    pinMode(SensorEntrada1, INPUT);


    

    pinMode(SensorSaida2, OUTPUT);
    digitalWrite(SensorSaida2, LOW);
    delayMicroseconds(500);
    
    pinMode(SensorEntrada2, INPUT);

   
 
  
  
}

void loop() {
      
    digitalWrite(SensorSaida1, HIGH);
    delayMicroseconds(500);
    digitalWrite(SensorSaida1, LOW);

     tempo1 = pulseIn(SensorEntrada1, HIGH);
     distancia1 = tempo1 / 29.4 / 2;
    
    Serial.println("Distancia PESSOA");
    
    Serial.println(distancia1);

     if(distancia1 < 150){

          servo_13.write(0);

             delay(500);
      
      }else
      {
          servo_13.write(120);
         
       
      }

    digitalWrite(SensorSaida2, HIGH);
    delayMicroseconds(500);
    digitalWrite(SensorSaida2, LOW);

    tempo2 = pulseIn(SensorEntrada2, HIGH);
    distancia2 = tempo2 / 29.4 / 2;

  
      if(distancia2 >29){

    lcd.setCursor(0, 0);
    lcd.print("   LIXEIRA ");
    lcd.setCursor(1, 0);
    lcd.print("   VAZIA ");
      }
     delay (5000);

      if(distancia2 >25){

    lcd.setCursor(0, 0);
    lcd.print(" VOLUME DE LIXO");
    lcd.setCursor(0, 1);
    lcd.print("      90%     ");
      }
       delay (5000);
     if(distancia2 >22,4){

    lcd.setCursor(0, 0);
    lcd.print(" VOLUME DE LIXO");
    lcd.setCursor(0, 1);
    lcd.print("      80%     ");
      }
    delay (5000);   
      if(distancia2 >19,6){

    lcd.setCursor(0, 0);
    lcd.print(" VOLUME DE LIXO");
    lcd.setCursor(0, 1);
    lcd.print("      70%     ");
      }
delay (5000);
      if(distancia2 >16,8){

    lcd.setCursor(0, 0);
    lcd.print(" VOLUME DE LIXO");
    lcd.setCursor(0, 1);
    lcd.print("      60%     ");
      }
    delay (5000);  
      if(distancia2 >14){

    lcd.setCursor(0, 0);
    lcd.print(" VOLUME DE LIXO");
    lcd.setCursor(0, 1);
    lcd.print("      50%     ");
      }
 delay (5000);
      if(distancia2 >11,2){

    lcd.setCursor(0, 0);
    lcd.print(" VOLUME DE LIXO");
    lcd.setCursor(0, 1);
    lcd.print("      40%     ");
      }
 delay (5000);
      if(distancia2 >8,4){

    lcd.setCursor(0, 0);
   lcd.print(" VOLUME DE LIXO");
    lcd.setCursor(0, 1);
    lcd.print("      30%     ");
      }
   delay (5000);    
        if(distancia2 >5,6){

    lcd.setCursor(0, 0);
    lcd.print(" VOLUME DE LIXO");
    lcd.setCursor(0, 1);
    lcd.print("      20%     ");
      }
 delay (5000);
     if(distancia2 >2,8 ){

    lcd.setCursor(0, 0);
    lcd.print(" VOLUME DE LIXO");
    lcd.setCursor(0, 1);
    lcd.print("      10%     ");
      }
delay (5000);


    Serial.println("Distancia FUNDO");
    Serial.println(distancia2);
    delay(2000);
     
}
