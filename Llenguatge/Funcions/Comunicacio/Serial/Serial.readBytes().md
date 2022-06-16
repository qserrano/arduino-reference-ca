---
títol: "Serial.readBytes()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.readBytes()

### Descripció

`Serial.readBytes()` llig caràcters del port serie en un búfer. La funció finalitza si s'ha llegit la longitud determinada o s'esgota el temps d'espera (veure `Serial.setTimeout()`).

`Serial.readBytes()` retorna el nombre de caràcters col·locats en el búfer. Un 0 significa que no es van trobar dades vàlides.

`Serial.readBytes()` hereta de la classe d'utilitat [stream](../Stream.md).

### Sintaxi

`Serial.readBytes (buffer, length)`

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Sèrie.  
`buffer`: el búfer per a emmagatzemar els bytes. Tipus de dades permeses: array of char o byte.  
`length`: el nombre de bytes a llegir. Tipus de dades permeses: int.  

### Devolucions

El nombre de bytes col·locats en el búfer. Tipus de dades: size_t.

### Vegeu també

LLENGUATGE [Serial.setTimeout()](./Serial.setTimeout().md)  
LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
