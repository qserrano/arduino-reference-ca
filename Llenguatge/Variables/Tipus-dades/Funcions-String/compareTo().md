---
títol: "compareTo()"
categoria: [ "Variables" ]
subcategoria: [ "Tipus de dades" ]
subfunció: ["String()"]
---

# compareTo()

## Descripció

Compara dues cadenes, provant si una ve abans o després de l'altra, o si són iguals. Les cadenes es comparen caràcter per caràcter, utilitzant els valors ASCII dels caràcters. Això vol dir, per exemple, que "a" ve abans de "b" però després de "A". Els números van abans de les lletres.

## Sintaxi

`myString.compareTo(myString2)`

## Paràmetres

`myString`: una variable de tipus String.  
`myString2`: una altra variable de tipus String.

## Devolucions

un nombre negatiu: si myString arriba abans de myString2.
0: si String és igual a myString2.  
un nombre positiu: si myString ve després de myString2.

## Vegeu també

EXEMPLE [Tutorials de cadenes](https://www.arduino.cc/en/Tutorial/BuiltInExamples#strings) (en anglés)  
LLENGUATGE [String()](../String().md)
