---
títol: "Stream.parseInt()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Stream"
---

# Stream.parseInt()

### Descripció

`parseInt()` retorna el primer nombre enter vàlid (llarg) de la posició actual.

En particular:

- L'anàlisi s'atura quan no s'ha llegit cap caràcter per a un valor de temps d'espera configurable, o quan es llegeix un dígit que no és;
- Si no es van llegir dígits vàlids quan es produeix el temps d'espera (vegeu [Stream.setTimeout()](./Stream.setTimeout().md)), es retorna 0;

Aquesta funció forma part de la classe Stream i pot ser cridada per qualsevol classe que en hereti (Wire, Serial, etc.). Consulteu la pàgina principal de la classe [Stream](../Stream.md) per obtenir més informació.

### Sintaxi

`stream.parseInt()`  
`stream.parseInt(lookahead)`  
`stream.parseInt(lookahead, ignore)`  

### Paràmetres

`stream` : una instància d'una classe que hereta de Stream.  
`lookahead`: el mode utilitzat per mirar endavant al flux d'un nombre enter. Tipus de dades permesos:  
 LookaheadMode. Valors permesos:
  - SKIP_ALL: tots els caràcters que no siguin els dígits o el signe menys s'ignoren quan s'escaneja el flux per trobar un nombre enter. Aquest és el mode predeterminat.
  - SKIP_NONE: no es salta res i no es toca el flux tret que el primer caràcter d'espera sigui vàlid.
  - SKIP_WHITESPACE: només s'ometen les tabulacions, els espais, els passos de línia i els retorns de carro.
`ignore`: s'utilitza per saltar el caràcter indicat a la cerca. S'utilitza, per exemple, per saltar el divisor de milers. Tipus de dades permesos: char  

### Devolucions

Tipus de dades: long.

### Vegeu també

LLENGUATGE [Stream](../Stream.md)  
LLENGUATGE [Funcions](../../Funcions.md)  
