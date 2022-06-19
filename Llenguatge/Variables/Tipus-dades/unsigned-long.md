---
títol: "unsigned-long"
categories: [ "Variables" ]
subcategories: [ "Tipus de dades" ]
---

# unsigned long

## Descripció

Les variables llargues sense signar són variables de mida ampliada per a l'emmagatzematge de números i emmagatzemen 32 bits (4 bytes). A diferència dels llargs estàndard, els llargs sense signe no emmagatzemaran nombres negatius, de manera que el seu interval va de 0 a 4.294.967.295 (2^32 - 1).

## Sintaxi

`unsigned long var = val;`

## Paràmetres

`var`: nom de variable.  
`val`: el valor que assigneu a aquesta variable.

## Exemple de codi

```
unsigned long time;

void setup() {
  Serial.begin(9600);
}

void loop() {
  Serial.print("Time: ");
  time = millis();
  //prints time since program started
  Serial.println(time);
  // wait a second so as not to send massive amounts of data
  delay(1000);
}
```

## Vegeu també

LLENGUATGE [Constants enteres](../Constants/constants-enteres.md)  
LLENGUATGE [Variables](../../Variables.md)
