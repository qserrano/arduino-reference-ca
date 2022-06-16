---
títol: "Stream.readBytesUntil()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Stream"
---

# Stream.readBytesUntil()

### Descripció

`readBytesUntil()` llegeix caràcters d'un flux a un buffer. La funció finalitza si es detecta el caràcter de terminació, s'ha llegit la longitud determinada o s'esgota el temps d'espera (vegeu [Stream.setTimeout()](./Stream.setTimeout().md)). La funció retorna els caràcters fins a l'últim caràcter abans del terminador subministrat. El propi terminador no es retorna a la memòria intermèdia.

`readBytesUntil()` retorna el nombre de bytes col·locats a la memòria intermèdia. Un 0 significa que no s'han trobat dades vàlides.

Aquesta funció forma part de la classe Stream i pot ser cridada per qualsevol classe que en hereti (Wire, Serial, etc.). Consulteu la pàgina principal de la classe [Stream](../Stream.md) per obtenir més informació.

### Sintaxi

`stream.readBytesUntil(character, buffer, length)`

### Paràmetres

`stream`: una instància d'una classe que hereta de Stream.  
`character`: el caràcter a buscar. Tipus de dades permesos: char.  
`buffer`: la memòria intermèdia on emmagatzemar els bytes. Tipus de dades permesos: array of char o bytes.  
`length`: el nombre de bytes a llegir. Tipus de dades permesos: int.  

### Devolucions

El nombre de bytes col·locats a la memòria intermèdia.

### Notes i advertències

El caràcter de terminació es descarta del flux.

### Vegeu també

LLENGUATGE [Stream](../Stream.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
