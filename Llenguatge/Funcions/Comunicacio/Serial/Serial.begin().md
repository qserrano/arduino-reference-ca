---
títol: "Serial.begin()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Serial"
---

# Serial.begin()

### Descripció

Estableix la velocitat de dades en bits per segon (bauds) per a la transmissió de dades en sèrie. Per a comunicar-se amb Serial Monitor, assegure's d'usar una de les velocitats en bauds enumerades en el menú a la cantonada inferior dreta de la seua pantalla. No obstant això, pot especificar altres velocitats, per exemple, per a comunicar-se a través dels pins 0 i 1 amb un component que requereix una velocitat en bauds particular.

Un segon argument opcional configura els bits de dades, paritat i parada. El valor predeterminat és 8 bits de dades, sense paritat, un bit de parada.

### Sintaxi

`Serial.begin(speed)`  
`Serial.begin(speed, config)`  

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Serial.  
`speed`: en bits per segon (bauds). Tipus de dades permeses: llargs.  
`config`: estableix dades, paritat i bits de parada. Els valors vàlids són:  

  * SERIAL_5N1  
  * SERIAL_6N1  
  * SERIAL_7N1  
  * SERIAL_8N1 (the default)  
  * SERIAL_5N2  
  * SERIAL_6N2  
  * SERIAL_7N2  
  * SERIAL_8N2  
  * SERIAL_5E1: even parity  
  * SERIAL_6E1  
  * SERIAL_7E1  
  * SERIAL_8E1  
  * SERIAL_5E2  
  * SERIAL_6E2  
  * SERIAL_7E2  
  * SERIAL_8E2  
  * SERIAL_5O1: odd parity  
  * SERIAL_6O1  
  * SERIAL_7O1  
  * SERIAL_8O1  
  * SERIAL_5O2  
  * SERIAL_6O2  
  * SERIAL_7O2  
  * SERIAL_8O2  

### Devolucions

Cap

### Codi d'exemple

```
void setup() {
    Serial.begin(9600); // opens serial port, sets data rate to 9600 bps
}

void loop() {}
Arduino Mega example:
// Arduino Mega using all four of its Serial ports
// (Serial, Serial1, Serial2, Serial3),
// with different baud rates:

void setup() {
  Serial.begin(9600);
  Serial1.begin(38400);
  Serial2.begin(19200);
  Serial3.begin(4800);

  Serial.println("Hello Computer");
  Serial1.println("Hello Serial 1");
  Serial2.println("Hello Serial 2");
  Serial3.println("Hello Serial 3");
}
void loop() {}
```

### Notes i Advertiments

Per als ports serials USB CDC (per exemple, Serial en Leonardo), `Serial.begin()` és irrellevant. Pot utilitzar qualsevol velocitat de transmissió i configuració per a la comunicació en sèrie amb aquests ports. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Serial.

L'únic valor de configuració compatible amb Serial1 en les plaques Arduino Nano 33 BLE i Nano 33 BLE Sense és SERIAL_8N1.

### Vegeu també

LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)  
