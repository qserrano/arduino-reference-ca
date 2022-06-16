---
títol: "Stream.readStringUntil()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Stream"
---

# Stream.readStringUntil()

### Descripció

`readStringUntil()` llegeix caràcters d'un flux a una cadena. La funció s'acaba si es detecta el caràcter de terminació o s'esgota el temps (vegeu [Stream.setTimeout()](./Stream.setTimeout().md)).

Aquesta funció forma part de la classe Stream i pot ser cridada per qualsevol classe que en hereti (Wire, Serial, etc.). Consulteu la pàgina principal de la classe [Stream](../Stream.md) per obtenir més informació.

### Sintaxi

`stream.readStringUntil(terminator)`

### Paràmetres

`stream`: una instància d'una classe que hereta de Stream.  
`terminator`: el caràcter a cercar. Tipus de dades permesos: char.  

### Devolucions

Tota la cadena es llegeix des d'un flux, fins al caràcter de terminació

### Notes i advertències

El caràcter de terminació es descarta del flux.

### Vegeu també

LLENGUATGE [Stream](../Stream.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
