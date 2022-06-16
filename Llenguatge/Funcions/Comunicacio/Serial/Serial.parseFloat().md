---
títol: "Serial.parseFloat()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.parseFloat()

### Descripció

`Serial.parseFloat()` retorna el primer número de coma flotant vàlid del búfer.  `Serial.parseFloat()` acaba amb el primer caràcter que no és un número de punt flotant. La funció finalitza si s'esgota el temps d'espera (veure `Serial.setTimeout()`).

`Serial.parseFloat()` hereta de la classe d'utilitat [stream](../Stream.md).

### Sintaxi

`Serial.parseFloat()`  
`Serial.parseFloat (lookahead)`  
`Serial.parseFloat (lookahead, ignore)`  

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal [Serial](../Serial.md).  
`lookahead`: la manera utilitzada per a mirar cap avant en el flux d'un número de punt flotant. Tipus de dades permeses: LookaheadMode. Valors lookahead permesos:
  *  SKIP_ALL: tots els caràcters que no siguen el signe menys, el punt decimal o els dígits s'ignoren en escanejar la transmissió a la recerca d'un número de punt flotant. Aquest és la manera per defecte.
  *  SKIP_NONE: no se salta res i la seqüència no es toca llevat que el primer caràcter d'espera siga vàlid.
  *  SKIP_WHITESPACE: només se salten tabulacions, espais, salts de línia i retorns de carro.
`ignore`: s'utilitza per a ometre el caràcter indicat en la cerca. S'utilitza, per exemple, per a ometre el divisor de milers. Tipus de dades permeses: char

### Devolucions

Tipus de dada: float.

### Vegeu també

LLENGUATGE [Serial.setTimeout()](./Serial.setTimeout.md)  
LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
