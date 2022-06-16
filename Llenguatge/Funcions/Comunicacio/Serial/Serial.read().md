---
títol: "Serial.read()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.read()

### Descripció

Llig les dades serials entrants.

`Serial.read()` hereta de la classe d'utilitat [stream](../Stream.md).

### Sintaxi

`Serial.read()`

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Serial.

### Devolucions

El primer byte de dades en sèrie entrants disponibles (o -1 si no hi ha dades disponibles). Tipus de dada: int.

### Codi d'exemple

```
int incomingByte = 0; // for incoming serial data

void setup() {
  Serial.begin(9600); // opens serial port, sets data rate to 9600 bps
}

void loop() {
  // send data only when you receive data:
  if (Serial.available() > 0) {
    // read the incoming byte:
    incomingByte = Serial.read();

    // say what you got:
    Serial.print("I received: ");
    Serial.println(incomingByte, DEC);
  }
}
```

### Vegeu també

LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
