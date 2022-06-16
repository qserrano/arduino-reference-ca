---
títol: "Stream.readBytes()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Stream"
---

# Stream.readBytes()

### Descripció

`readBytes()` llegeix caràcters d'un flux a un buffer. La funció s'acaba si s'ha llegit la longitud determinada, o s'esgota el temps d'espera (vegeu [Stream.setTimeout()](./Stream.setTimeout().md)).

`readBytes()` retorna el nombre de bytes col·locats a la memòria intermèdia. Un 0 significa que no s'han trobat dades vàlides.

Aquesta funció forma part de la classe Stream i pot ser cridada per qualsevol classe que en hereti (Wire, Serial, etc.). Consulteu la pàgina principal de la classe [Stream](../Stream.md) per obtenir més informació.

### Sintaxi

`stream.readBytes (buffer, length)`

### Paràmetres

`stream`: una instància d'una classe que hereta de Stream.  
`buffer`: la memòria intermèdia on emmagatzemar els bytes. Tipus de dades permesos: array of char o bytes.  
`length`: el nombre de bytes a llegir. Tipus de dades permesos: int.  

### Devolucions

El nombre de bytes col·locats a la memòria intermèdia. Tipus de dades: size_t.

### Vegeu també

LLENGUATGE [Stream](../Stream.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
