---
títol: "Serial.peek()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.peek()

### Descripció

Retorna el següent byte (caràcter) de les dades serials entrants sense eliminar-los del búfer serial intern. És a dir, les crides successives a `peek()` retornaran el mateix caràcter, igual que la següent crida a `read()`.

`Serial.peek()` hereta de la classe d'utilitat [stream](../Stream.md).

### Sintaxi

`Serial.peek()`

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Sèrie.

### Devolucions

El primer byte de les dades serials entrants disponibles (o -1 si no hi ha dades disponibles). Tipus de dada: int.

### Vegeu també

LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
