---
títol: ">"
descripció: ["Més gran que"]
categoria: [ "Variables" ]
subcategoria: [ "Tipus de dades" ]
subfunció: ["String()"]
---

# >

## Descripció

Comprova si la cadena de l'esquerra és més gran que la cadena de la dreta. Aquest operador avalua les cadenes en ordre alfabètic, en el primer caràcter on els dos difereixen. Així, per exemple, "b" > "a" i "2" > "1", però "999" > "1000" perquè 9 ve després d'1.

**Precaució**: els operadors de comparació de cadenes poden ser confusos quan compareu cadenes numèriques, perquè els números es tracten com a cadenes i no com a números. Si necessiteu comparar números numèricament, compareu-los com a enters, flotants o llargs, i no com a cadenes.

## Sintaxi

`myString1 > myString2`

## Paràmetres

`myString1`: una variable de cadena  
`myString2`: una variable de cadena

## Devolucions

true: si myString1 és més gran que myString2  
fals: en cas contrari.

## Vegeu també

EXEMPLE [Tutorials de cadenes](https://www.arduino.cc/en/Tutorial/BuiltInExamples#strings) (en anglés)  
LLENGUATGE [String()](../String().md)
