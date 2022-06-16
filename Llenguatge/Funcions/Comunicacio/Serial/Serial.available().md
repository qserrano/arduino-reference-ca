---
títol: "Serial.available()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Serial"
---

# Serial.available()

### Descripció

Obté la quantitat de bytes (caràcters) disponibles per a llegir des d'un port serie. Aquests dades ja van arribar i es van emmagatzemar en el búfer de recepció en sèrie (que soporta 64 bytes).

`Serial.available()` hereta de la classe d’utilitat Stream.

### Sintaxi

`Serial.available()`

### Paràmetres

`Serial` objecte de port serie. Consulteu la llista de ports serie disponibles per a cada placa en la pàgina principal Serial.

### Devolucions

el nombre de bytes disponibles per a llegir

### Codi d’exemple
```
// include the SoftwareSerial library so you can use its functions:
#include <SoftwareSerial.h>

#define rxPin 10
#define txPin 11

// set up a new serial port
SoftwareSerial mySerial =  SoftwareSerial(rxPin, txPin);

void setup()  {
  // define pin modes for tx, rx:
  pinMode(rxPin, INPUT);
  pinMode(txPin, OUTPUT);
  // set the data rate for the SoftwareSerial port
  mySerial.begin(9600);
}

void loop() {
  if (mySerial.available()>0){
  mySerial.read();
 }
}
```

### Vegeu també

LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)  
