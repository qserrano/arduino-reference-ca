---
títol: "Serial.parseInt()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.parseInt()

### Descripció

Cerca el següent enter vàlid en la sèrie entrant. La funció finalitza si s'esgota el temps d'espera (veure `Serial.setTimeout()`).

`Serial.parseInt()` hereta de la classe d'utilitat [stream](../Stream.md).

En particular:
- L'anàlisi es deté quan no s'han llegit caràcters per a un valor de temps d'espera configurable, o si es llig un caràcter no numeric;
- Si no s’han llegit dígits vàlids quan es va esgotar el temps d'espera (consulte `Serial.setTimeout()`), es retorna 0;

### Sintaxi

`Serial.parseInt()`  
`Serial.parseInt (lookahead)`  
`Serial.parseInt(lookahead, ignore)`  

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Sèrie.
`lookahead`: la manera utilitzada per a mirar cap avant en la seqüència d'un nombre enter. Tipus de dades permeses: LookaheadMode. Valors lookahead permesos:
  *  SKIP_ALL: tots els caràcters que no siguen dígits o un signe menys s'ignoren en escanejar la seqüència a la recerca d'un nombre enter. Aquest és la manera per defecte.
  *  SKIP_NONE: no se salta res i la seqüència no es toca llevat que el primer caràcter d'espera siga vàlid.
  *  SKIP_WHITESPACE: només se salten tabulacions, espais, salts de línia i retorns de carro.
`ignore`: s'utilitza per a ometre el caràcter indicat en la cerca. S'utilitza, per exemple, per a ometre el divisor de milers. Tipus de dades permeses: char

### Devolucions

El següent enter vàlid. Tipus de dada: long.

### Vegeu també

LLENGUATGE [Serial.setTimeout()](./Serial.setTimeout.md)  
LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
