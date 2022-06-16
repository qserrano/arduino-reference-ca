---
títol: "Stream.peek()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Stream"
---

# Stream.peek()

### Descripció

Llegeix un byte del fitxer sense avançar al següent. És a dir, les crides successives a `peek() `retornaran el mateix valor, igual que la següent crida a `read()`.

Aquesta funció forma part de la classe Stream i pot ser cridada per qualsevol classe que en hereti (Wire, Serial, etc.). Consulteu la pàgina principal de la classe [Stream](../Stream.md) per obtenir més informació.

### Sintaxi

`stream.peek()`

### Paràmetres

`stream`: una instància d'una classe que hereta de Stream.

### Devolucions

El següent byte (o caràcter), o -1 si no n'hi ha cap disponible.

### Vegeu també

LLENGUATGE [Stream](../Stream.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
