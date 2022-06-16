---
títol: "Serial.print()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.print()

### Descripció

Imprimeix dades en el port serial com a text ASCII llegible per humans. Aquest comando pot prendre moltes formes. Els números s'imprimeixen utilitzant un caràcter ASCII per a cada dígit. Els flotants s'imprimeixen de manera similar com a dígits ASCII, per defecte amb dos decimals. Els bytes s'envien com un sol caràcter. Els caràcters i les cadenes s'envien tal qual. Per exemple:

* Serial.print(78) dona "78"
* Serial.print(1.23456) dona "1.23"
* Serial.print('N') dona "N"
* Serial.print("Hola món") dona "Hola món".

Un segon paràmetre opcional especifica la base (format) a usar; els valors permesos són BIN (binari o base 2), OCT (octal o base 8), DEC (decimal o base 10), HEX (hexadecimal o base 16). Per a números de punt flotant, aquest paràmetre especifica el nombre de llocs decimals que s'usaran. Per exemple:

* Serial.print(78, BIN) dona "1001110"
* Serial.print(78, OCT) dona "116"
* Serial.print(78, DEC) dona "78"
* Serial.print(78, HEX) dona "4E"
* Serial.print(1.23456, 0) dona "1"
* Serial.print(1.23456, 2) dona "1.23"
* Serial.print(1.23456, 4) dona "1.2345"

Pot passar cadenes basades en memòria flash a `Serial.print()` embolicant-les amb F(). Per exemple:

* `Serial.print(F("Hola Món"))`

Per a enviar dades sense conversió a la seua representació com a caràcters, use `Serial.write()`.

### Sintaxi

`Serial.print(val)`  
`Serial.print(val, format)`  

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Sèrie.  
`val`: el valor a imprimir. Tipus de dades permeses: qualsevol tipus de dades.

### Devolucions

`print()` retorna el nombre de bytes escrits, encara que llegir aqueix número és opcional. Tipus de dades: size_t.

### Codi d'exemple

```
/*
  Uses a for loop to print numbers in various formats.
*/
void setup() {
  Serial.begin(9600); // open the serial port at 9600 bps:
}

void loop() {
  // print labels
  Serial.print("NO FORMAT");  // prints a label
  Serial.print("\t");         // prints a tab

  Serial.print("DEC");
  Serial.print("\t");

  Serial.print("HEX");
  Serial.print("\t");

  Serial.print("OCT");
  Serial.print("\t");

  Serial.print("BIN");
  Serial.println();        // carriage return after the last label

  for (int x = 0; x < 64; x++) { // only part of the ASCII chart, change to suit
    // print it out in many formats:
    Serial.print(x);       // print as an ASCII-encoded decimal - same as "DEC"
    Serial.print("\t\t");  // prints two tabs to accomodate the label lenght

    Serial.print(x, DEC);  // print as an ASCII-encoded decimal
    Serial.print("\t");    // prints a tab

    Serial.print(x, HEX);  // print as an ASCII-encoded hexadecimal
    Serial.print("\t");    // prints a tab

    Serial.print(x, OCT);  // print as an ASCII-encoded octal
    Serial.print("\t");    // prints a tab

    Serial.println(x, BIN);  // print as an ASCII-encoded binary
    // then adds the carriage return with "println"
    delay(200);            // delay 200 milliseconds
  }
  Serial.println();        // prints another carriage return
}
```

### Notes i Advertiments

Per a obtindre informació sobre l'asincronia de `Serial.print()`, consulte la secció Notes i advertiments de la pàgina de referència de `Serial.write()`.

### Vegeu també

LLENGUATGE [Serial.write()](./Serial.write().md)  
LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
