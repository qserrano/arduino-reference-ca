---
títol: "Serial.readStringUntil()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.readStringUntil()

### Descripció

`readStringUntil()` llig caràcters del búfer serial en una cadena. La funció finalitza si s'esgota el temps d'espera (veure `setTimeout()`).

`Serial.readStringUntil()` hereta de la classe d'utilitat [stream](../Stream.md).

### Sintaxi

`Serial.readStringUntil(terminator)`

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Serial.  
`terminator`: el caràcter a buscar. Tipus de dades permeses: char.  

### Devolucions

La cadena completa es llig des del búfer en sèrie, fins al caràcter terminator

### Notes i Advertiments

El caràcter terminador es descarta del búfer serial.

### Vegeu també

LLENGUATGE [Serial.setTimeout()](./Serial.setTimeout().md)  
LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../Funcions.md)
