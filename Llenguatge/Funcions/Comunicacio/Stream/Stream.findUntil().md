---
títol: "Stream.findUntil()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Stream"
---

# Stream.findUntil()

### Descripció

`findUntil()` llegeix dades del flux fins que es troba la cadena de destinació d'una longitud determinada o una cadena de terminació, o s'espera (vegeu [Stream.setTimeout()](./Stream.setTimeout().md)).

La funció retorna true si es troba la cadena de destinació, false si s'ha esgotat el temps.

Aquesta funció forma part de la classe Stream i pot ser cridada per qualsevol classe que en hereti (Wire, Serial, etc.). Consulteu la pàgina principal de la classe [Stream](../Stream.md) per obtenir més informació.

### Sintaxi

`stream.findUntil(target, terminal)`  

### Paràmetres

`stream`: una instància d'una classe que hereta de Stream.  
`target`: la cadena a cercar. Tipus de dades permesos: char.  
`terminal`: la cadena de terminal a la cerca. Tipus de dades permesos: char.  

### Devolucions

Tipus de dades: bool.

### Vegeu també

LLENGUATGE [Stream](../Stream.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
