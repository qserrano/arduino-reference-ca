---
títol: "Serial.readBytesUntil()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.readBytesUntil()

### Descripció

`Serial.readBytesUntil()` llig caràcters del búfer serial en una matriu. La funció finalitza (les comprovacions es realitzen en aquest ordre) si s'ha llegit la longitud determinada, si s'esgota el temps d'espera (consulte `Serial.setTimeout()`) o si es detecta el caràcter de terminació (i en aquest cas, la funció retorna els caràcters fins a l'últim caràcter abans del terminador proporcionat). El terminador en si no es retorna en el búfer.

`Serial.readBytesUntil()` retorna el nombre de caràcters llegits en el búfer. Un 0 significa que el paràmetre de longitud es <= 0, es va esgotar el temps d'espera abans que qualsevol altra entrada o es va trobar un caràcter de terminació abans que qualsevol altra entrada.

`Serial.readBytesUntil()` hereta de la classe d'utilitat [stream](../Stream.md).

### Sintaxi

`Serial.readBytesUntil(character, buffer, length)`

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Sèrie.  
`character`: el caràcter a buscar. Tipus de dades permeses: char.  
`buffer`: el búfer per a emmagatzemar els bytes. Tipus de dades permeses: matriu de char o byte.  
`length`: el nombre de bytes a llegir. Tipus de dades permeses: int.  

### Devolucions

Tipus de dades: size_t.

### Notes i Advertiments

El caràcter terminador es descarta del búfer en sèrie, llevat que el nombre de caràcters llegits i copiats en el búfer siga igual a la longitud.

### Vegeu també

LLENGUATGE [Serial.setTimeout()](./Serial.setTimeout().md)  
LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
