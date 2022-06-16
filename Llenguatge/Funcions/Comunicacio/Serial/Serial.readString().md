---
títol: "Serial.readString()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.readString()

### Descripció

`Serial.readString()` llig caràcters del búfer serial en una cadena. La funció finalitza si s'esgota el temps d'espera (veure `Serial.setTimeout()`).

`Serial.readString()` hereta de la classe d'utilitat [stream](../Stream.md).

### Sintaxi

`Serial.readString()`

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Serial.

### Devolucions

Una cadena llegida del búfer serial

### Vegeu també

LLENGUATGE [Serial.setTimeout()](./Serial.setTimeout().md)  
LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
