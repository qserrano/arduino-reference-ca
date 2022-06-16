---
títol: "Serial.setTimeout()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.setTimeout()

### Descripció

`Serial.setTimeout()` estableix el màxim de mil·lisegons per a esperar les dades en sèrie. El valor predeterminat és 1000 mil·lisegons.

`Serial.setTimeout()` hereta de la classe d'utilitat [stream](../Stream.md).

### Sintaxi

`Serial.setTimeout(time)`

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Sèrie.  
`time`: duració del temps d'espera en mil·lisegons. Tipus de dades permeses: long.  

### Devolucions

Res

### Notes i Advertiments

Funcions serial que usen el valor de temps d'espera establit a través de `Serial.setTimeout()`:

- [Serial.find()](./Serial.find().md)
- [Serial.findUntil()](./Serial.findUntil().md)
- [Serial.parseInt()](./Serial.parseInt().md)
- [Serial.parseFloat()](./Serial.parseFloat().md)
- [Serial.readBytes()](./Serial.readBytes().md)
- [Serial.readBytesUntil()](./Serial.readBytesUntil().md)
- [Serial.readString()](./Serial.readString().md)
- [Serial.readStringUntil()](./Serial.readStringUntil().md)


### Vegeu també

LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../Funcions.md)
