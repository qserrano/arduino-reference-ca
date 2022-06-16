---
títol: "Wire.write()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Wire"
---

# write()

### Descripció

Aquesta funció escriu dades d'un dispositiu perifèric en resposta a una sol·licitud d'un dispositiu controlador, o posa en cua bytes per a la transmissió d'un controlador a un dispositiu perifèric (entre les trucades a `beginTransmission()` i `endTransmission()`).

### Sintaxi

`Wire.write(valor)`  
`Wire.write(cadena)`   
`Wire.write(dades, longitud)`  

### Paràmetres

`valor`: un valor per enviar com a únic byte.  
`cadena`: una cadena per enviar com una sèrie de bytes.  
`dades`: una matriu de dades per enviar com a bytes.  
`longitud`: el nombre de bytes a transmetre.  

### Devolucions

El nombre de bytes escrits (la lectura d'aquest número és opcional).

### Exemple

```
#include <Wire.h>

byte val = 0;

void setup() {
  Wire.begin(); // Join I2C bus
}

void loop() {
    Wire.beginTransmission(44);  // Transmit to device number 44 (0x2C)

    Wire.write(val);             // Sends value byte
    Wire.endTransmission();      // Stop transmitting

    val++;                       // Increment value

    // if reached 64th position (max)
    if(val == 64) {
        val = 0;                   // Start over from lowest value
    }

    delay(500);
}
```
### Vegeu també

LLENGUATGE [Wire](../wire.md)  
LLENGUATGE [Funcions](../../../Funcions.md)

