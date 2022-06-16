---
títol: "Serial.println()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.println()

### Descripció

Imprimeix dades en el port serie com a text ASCII llegible per humans seguit d'un caràcter de retorn de carro (ASCII 13 o '\r') i un caràcter de nova línia (ASCII 10 o '\n'). Aquest comando pren les mateixes formes que `Serial.print()`.

### Sintaxi

`Serial.println(val)`  
`Serial.println(val, format)`  

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Sèrie.  
`val`: el valor a imprimir. Tipus de dades permeses: qualsevol tipus de dades.  
`format`: especifica la base numèrica (per a tipus de dades integrals) o el nombre de llocs decimals (per a tipus de punt flotant).  

### Devolucions

`println()` retorna el nombre de bytes escrits, encara que llegir aqueix número és opcional. Tipus de dades: size_t.

### Codi d'exemple

```
/*
 Analog input reads an analog input on analog in 0, prints the value out.
 created 24 March 2006
 by Tom Igoe
 */

int analogValue = 0;    // variable to hold the analog value

void setup() {
  // open the serial port at 9600 bps:
  Serial.begin(9600);
}

void loop() {
  // read the analog input on pin 0:
  analogValue = analogRead(0);

  // print it out in many formats:
  Serial.println(analogValue);       // print as an ASCII-encoded decimal
  Serial.println(analogValue, DEC);  // print as an ASCII-encoded decimal
  Serial.println(analogValue, HEX);  // print as an ASCII-encoded hexadecimal
  Serial.println(analogValue, OCT);  // print as an ASCII-encoded octal
  Serial.println(analogValue, BIN);  // print as an ASCII-encoded binary

  // delay 10 milliseconds before the next reading:
  delay(10);
}
```

### Notes i Advertiments

Per a obtindre informació sobre l'asincronia de `Serial.println()`, consulte la secció Notes i advertiments de `Serial.write()`

### Vegeu també

LLENGUATGE [Serial.write()](./Serial.write().md)  
LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
