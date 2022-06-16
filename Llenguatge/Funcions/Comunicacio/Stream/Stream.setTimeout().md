---
títol: "Stream.setTimeout()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Stream"
---

# Stream.setTimeout()

### Descripció

`setTimeout()` estableix el màxim de mil·lisegons per esperar les dades del flux, el valor predeterminat és 1000 mil·lisegons. Aquesta funció forma part de la classe Stream i pot ser cridada per qualsevol classe que en hereti (Wire, Serial, etc.). Consulteu la pàgina principal de la classe [Stream](../Stream.md) per obtenir més informació.

### Sintaxi

`stream.setTimeout(time)`

### Paràmetres

`stream`: una instància d'una classe que hereta de Stream.  
`time`: temps d'espera en mil·lisegons. Tipus de dades permesos: long.  

### Devolucions

Res

### Notes i advertències

Funcions de flux que utilitzen el valor de temps d'espera establert mitjançant setTimeout():
- find()
- findUntil()
- parseInt()
- parseFloat()
- readBytes()
- readBytesUntil()
- readString()
- readStringUntil()

### Vegeu també

LLENGUATGE [Stream](../Stream.md)  
LLENGUATGE [Funcions](../../../Funcions.md)  
