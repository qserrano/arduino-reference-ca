---
títol: "delayMicroseconds()"
descripció: ""
categoria: "Funcions"
subcategoria: "Temps"
---

# delayMicroseconds()

### Descripció

Pausa el programa per la quantitat de temps (en microsegons) especificat pel paràmetre. Hi ha mil microsegons en un mil·lisegon i un milió de microsegons en un segon.

Actualment, el valor més gran que produirà un retard precís és 16383; valors més grans poden produir un retard extremadament curt. Això podria canviar en futures versions d'Arduino. Per a retards de més d'uns pocs milers de microsegons, ha d'usar `delay()` en el seu lloc.

### Sintaxi

`delayMicroseconds(us)`

### Paràmetres

`us`: el nombre de microsegons per a fer una pausa. Tipus de dades permeses: unsigned int.

### Devolucions

Res

### Codi d'exemple

El codi configura el pin número 8 perquè funcione com un pin d'eixida. Envia un tren de polsos d'aproximadament 100 microsegons de període. L'aproximació es deu a l'execució de les altres instruccions en el codi.

```
int outPin = 8;               // digital pin 8

void setup() {
  pinMode(outPin, OUTPUT);    // sets the digital pin as output
}

void loop() {
  digitalWrite(outPin, HIGH); // sets the pin on
  delayMicroseconds(50);      // pauses for 50 microseconds
  digitalWrite(outPin, LOW);  // sets the pin off
  delayMicroseconds(50);      // pauses for 50 microseconds
}
```

### Notes i Advertiments

Aquesta funció funciona amb molta precisió en el rang de 3 microsegons i fins a 16383. No podem assegurar que els microsegons de retard funcionen amb precisió per a temps de retard més xicotets. Els temps de retard més grans en realitat poden retardar per un temps extremadament breu.

A partir d'Arduino 0018, `delayMicroseconds()` ja no desactiva les interrupcions.

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
