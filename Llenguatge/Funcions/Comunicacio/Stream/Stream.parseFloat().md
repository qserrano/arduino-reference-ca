---
títol: "Stream.parseFloat()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Stream"
---

# Stream.parseFloat()

### Descripció

`parseFloat()` retorna el primer número de coma flotant vàlid des de la posició actual. `parseFloat()` acaba amb el primer caràcter que no és un nombre de coma flotant. La funció finalitza si s'esgota el temps d'espera (vegeu [Stream.setTimeout()](./Stream.setTimeout().md)).

Aquesta funció forma part de la classe Stream i pot ser cridada per qualsevol classe que en hereti (Wire, Serial, etc.). Consulteu la pàgina principal de la classe [Stream](../Stream.md) per obtenir més informació.

### Sintaxi

`stream.parseFloat()`  
`stream.parseFloat (lookahead)`  
`stream.parseFloat (lookahead, ignore)`  

### Paràmetres

`stream` : una instància d'una classe que hereta de Stream.  
`lookahead`: el mode que s'utilitza per mirar cap endavant al flux d'un nombre de coma flotant. Tipus de dades permesos: LookaheadMode. Valors permesos:
  - SKIP_ALL: tots els caràcters que no siguin el signe menys, el punt decimal o els dígits s'ignoren quan s'escanegen el flux per trobar un número de coma flotant. Aquest és el mode predeterminat.
  - SKIP_NONE: no es salta res i no es toca el flux tret que el primer caràcter d'espera sigui vàlid.
  - SKIP_WHITESPACE: només s'ometen les tabulacions, els espais, els passos de línia i els retorns de carro.

`ignore`: s'utilitza per saltar el caràcter indicat a la cerca. S'utilitza, per exemple, per saltar el divisor de milers. Tipus de dades permesos: char  

### Devolucions

Tipus de dades: float.

### Vegeu també

LLENGUATGE [Stream](../Stream.md)  
LLENGUATGE [Funcions](../../Funcions.md)  
