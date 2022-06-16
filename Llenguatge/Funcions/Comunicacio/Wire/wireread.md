---
títol: "Wire.read()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Wire"
---

# read()

### Descripció

Aquesta funció llegeix un byte que s'ha transmès des d'un dispositiu perifèric a un dispositiu controlador després d'una crida a `requestFrom()` o que s'ha transmès des d'un dispositiu controlador a un dispositiu perifèric. `read()` hereta de la classe d'utilitat Stream.

### Sintaxi

`Wire.read()`

### Paràmetres

Cap.

### Devolucions

El següent byte rebut.

### Exemple

#include <Wire.h>

void setup() {
  Wire.begin();             // Join I2C bus (address is optional for controller device)
  Serial.begin(9600);       // Start serial for output
}

void loop() {
    Wire.requestFrom(2, 6);    // Request 6 bytes from slave device number two

    // Slave may send less than requested
    while(Wire.available()) {
        char c = Wire.read();    // Receive a byte as character
        Serial.print(c);         // Print the character
    }

    delay(500);
}

### Vegeu també

LLENGUATGE [Wire](../wire.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
