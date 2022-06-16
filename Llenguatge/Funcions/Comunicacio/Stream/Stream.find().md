---
títol: "Stream.find()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Stream"
---

# Stream.find()

### Descripció

`find()` llegeix dades del flux fins que es troba l'objectiu. La funció retorna true si es troba l'objectiu, false si s'ha esgotat el temps (vegeu [Stream.setTimeout()](./Stream.setTimeout().md)).

Aquesta funció forma part de la classe Stream i pot ser cridada per qualsevol classe que en hereti (Wire, Serial, etc.). Consulteu la pàgina principal de la classe [Stream](../Stream.md) per obtenir més informació.

### Sintaxi

`stream.find (target)`  
`stream.find (target, length)`  

### Paràmetres

`stream`: una instància d'una classe que hereta de Stream.  
`target`: la cadena a cercar. Tipus de dades permesos: char.  
`length`: longitud de l'objectiu. Tipus de dades permesos: size_t.  

### Devolucions

Tipus de dades: bool.

### Vegeu també

LLENGUATGE [Stream](../Stream.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
