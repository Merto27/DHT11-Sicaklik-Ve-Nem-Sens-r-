# DHT11-Sicaklik-Ve-Nem-Sens-r-
#include <dht11.h> 
 
int DHT11_pin=2; 
dht11 DHT11_sensor; 
 
void setup()
{
  Serial.begin(9600); 
}
 
void loop()
{
  
 
  int chk = DHT11_sensor.read(DHT11_pin);
 
 
  Serial.print("Nem Orani (%): ");
  Serial.println((float)DHT11_sensor.humidity, 2);
 
  Serial.print("Sicaklik (Celcius): ");
  Serial.println((float)DHT11_sensor.temperature, 2);
 
  Serial.print("Sicaklik (Kelvin): ");
  Serial.println(DHT11_sensor.kelvin(), 2);
  
  Serial.print("Sicaklik (Fahrenheit): ");
  Serial.println(DHT11_sensor.fahrenheit(), 2);
 

  delay(2000);
 while(1);
}
