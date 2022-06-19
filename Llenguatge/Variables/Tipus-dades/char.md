---
títol: "char"
categories: [ "Variables" ]
subcategories: [ "Tipus de dades" ]
---

# char

## Descripció

Un tipus de dades utilitzat per a emmagatzemar un valor de caràcter. Els caràcters literals s'escriuen entre cometes simples, així: 'A' (per a diversos caràcters, cadenes, use cometes dobles: "ABC").

No obstant això, els caràcters s'emmagatzemen com a números. Pot veure la codificació específica en el gràfic ASCII. Això significa que és possible fer operacions aritmètiques amb caràcters, en les quals s'utilitza el valor ASCII del caràcter (per exemple, 'A' + 1 té el valor 66, ja que el valor ASCII de la lletra A majúscula és 65). Consulte la referència de `Serial.println` per a obtindre més informació sobre com els caràcters es tradueixen a números.

La grandària de la mena de dades char és d'almenys 8 bits. Es recomana usar char només per a emmagatzemar caràcters. Per a una mena de dades d'un byte (8 bits) sense signe, utilitze el tipus de dades byte.

## Sintaxi

`char var = valor;`

## Paràmetres

`var`: nom de la variable.  
`val`: el valor a assignar a aqueixa variable.

## Codi d'exemple

```
char miChar = 'A';
char miChar = 65; // tots dos són equivalents
```

## Veure també

LLENGUATGE [Serial.println](../../Funcions/Comunicacio/Serial/Serial.println().md)  
LLENGUATGE [char()](../Conversio/char().md)  
LLENGUATGE [Variables](../../Variables.md)
