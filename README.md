# PR-CTICA-2
Practica ESP32 con DHT11
En este repositorio se muestra como usando la plataforma Wokwi programando una ESP32 con el sensor DHT11.

Introducción

Descripción

La Esp32 la utilizamos en un entorno de adquision de datos, lo cual en esta practica ocuparemos un sensor (DTH11) para adquirir temperatura y humedad del entorno; Cabe aclarar que esta practica se usara un simulador llamado WOKWI.

Material Necesario

Para realizar esta practica necesitas lo siguiente: ºWOKWI ºTarjeta ESP 32 ºSensor DHT11

Instrucciones

Requisitos previos Para poder usar este repositorio necesitas entrar a la plataforma WOKWI.

Instrucciones de preparación de entorno

1.Abrir la terminal de programación y colocar la siguente programación:
-#include "DHTesp.h" -#include <LiquidCrystal_I2C.h>

-const int DHT_PIN = 15; -DHTesp dhtSensor;

void setup() {

Serial.begin(115200); dhtSensor.setup(DHT_PIN, DHTesp::DHT22); }

void loop() {

TempAndHumidity data = dhtSensor.getTempAndHumidity(); Serial.println("Temp: " + String(data.temperature, 1) + "°C"); Serial.println("Humidity: " + String(data.humidity, 1) + "%"); Serial.println("---"); delay(1000); }


2.Instalar la libreria de DHT sensor library for ESPx como se muestra en la siguente imagen.

![Captura de pantalla 2024-01-19 114027](https://github.com/robertopatino42/PR-CTICA-2/assets/153964688/7af1c32f-56ef-4d62-8d63-499e38a70032)

-Hacer la conexion de DHT11 con la ESP32 como se muestra en la siguente imagen.

![Captura de pantalla 2024-01-19 114056](https://github.com/robertopatino42/PR-CTICA-2/assets/153964688/1563e89b-29e2-4537-919f-a4cca5b12988)

Instrucciónes de operación Iniciar simulador. Visualizar los datos en el monitor serial. Colocar la temperatura y humedad dando doble click al sensor DHT11 Resultados

Cuando haya funcionado, verás los valores dentro del monitor serial como se muestra en la siguente imagen:

![Captura de pantalla 2024-01-19 114904](https://github.com/robertopatino42/PR-CTICA-2/assets/153964688/e70c42f1-4d2a-4c91-b562-49dd0cffc8b5)





