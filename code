#include <WiFi.h>
#include <LiquidCrystal_I2C.h>
#include "DHT.h"

WiFiClient client;

String thingSpeakAddress= "-----------";
String tsfield1Name;
String request_string;
String apiKey="----------";

DHT dht12(32,DHT11);
LiquidCrystal_I2C lcd(0x27,16,2); 
void setup()
{
Serial.begin(9600);
lcd.init();//Defining 16 columns and 2 rows of lcd display
delay(500);
lcd.backlight();
pinMode(4, INPUT);
  WiFi.disconnect();
  delay(3000);
  Serial.println("START");
  WiFi.begin("hi","987654321");
  while ((!(WiFi.status() == WL_CONNECTED))){
    delay(300);
    Serial.print("..");

  }
  Serial.println("Connected");
  Serial.println("Your IP is");
  Serial.println((WiFi.localIP()));
  lcd.setCursor(0,0);
  lcd.print("Welcome...");

}
void loop()
{   
    float Value= analogRead(34);
    float voltage=Value*(3.3/4095.0);
    float ph=(3.3*voltage);
    int sensorValue = analogRead(35);// read the input on analog pin A0:
    float volt = sensorValue * (5.0 / 1024.0); // Convert the analog reading (which goes from 0 - 1023) to a voltage (0 - 5V):
    delay(1000);
    float temp=dht12.readTemperature( );
    delay(1500);
    float humi=dht12.readHumidity();
    delay(1500);
    if (client.connect("api.thingspeak.com",80)) {
      Serial.println("Connected Successfully");
      request_string = thingSpeakAddress;
      request_string += "&field1=";
      request_string += ph;
      request_string += "&field2=";
      request_string += volt;
      request_string += "&field3=";
      request_string += temp;
      request_string += "&field4=";
      request_string += humi;
      client.print("POST /update HTTP/1.1\n");
      client.print("Host: api.thingspeak.com\n");
      client.print("Connection: close\n");
      client.print("X-THINGSPEAKAPIKEY: "+apiKey+"\n");
      client.print("Content-Type: application/x-www-form-urlencoded\n");
      client.print("Content-Length: ");
      client.print(request_string.length());
      client.print("\n\n");
      client.print(request_string);
      Serial.println("Ph:");
      Serial.println(ph,2);
      Serial.println("Turbidity:");
      Serial.println(volt,2);
      Serial.println("Temparature:");
      Serial.println(temp,2);
      Serial.println("Humidity");
      Serial.println(humi,2);
      lcd.setCursor(0,0); //Defining positon to write from first row,first column .
      lcd.print(" Ph:");
      lcd.print(ph,2); //You can write 16 Characters per line .                             
      lcd.setCursor(0,1);  //Defining positon to write from second row,first column .
      lcd.print("Turb:");
      lcd.print(volt,2);
      delay(3000); 

      lcd.clear();
      lcd.setCursor(0,0); //Defining positon to write from first row,first column .
      lcd.print("Temp:");
      lcd.print(temp,2); //You can write 16 Characters per line .
      lcd.setCursor(0,1);  //Defining positon to write from second row,first column .
      lcd.print("Humi:");
      lcd.print(humi),2;
      delay(3000); 
    

    } else {
      Serial.println("connection not available..! please enter the valid ssid and password");

    }
    if (ph == (random(6.5,8)) && volt == (random(10,20))) {
      Serial.println("The Quality of the Water is Good");
      
      lcd.clear();
      lcd.setCursor(0,0);
      lcd.print("Water is Good");
      delay(3000);

    } else {
      Serial.println("The Quality of Water is not good");
      lcd.clear();
      lcd.setCursor(0,0);
      lcd.print("Water is Bad");
      delay(3000);


    }
    delay(3000);

}
