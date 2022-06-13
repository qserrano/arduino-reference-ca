---
títol: "c_str()"
categoria: [ "Variables" ]
subcategoria: [ "Tipus de dades" ]
subfunció: ["String()"]
---

# c_str()

## Descripció

Converteix el contingut d'una cadena en una cadena d'estil C, amb terminació null. Tingueu en compte que això dóna accés directe a la memòria intermèdia interna de String i s'ha d'utilitzar amb cura. En particular, no hauríeu de modificar mai la cadena a través del punter retornat. Quan modifiqueu l'objecte String, o quan es destrueix, qualsevol punter retornat prèviament per c_str() esdevé invàlid i ja no s'hauria d'utilitzar.

## Sintaxi

`myString.c_str()`

## Paràmetres

`myString`: una variable de tipus String.

## Devolucions

Un punter a la versió d'estil C de la cadena invocadora.

## Vegeu també

EXEMPLE [Tutorials de cadenes](https://www.arduino.cc/en/Tutorial/BuiltInExamples#strings) (en anglés)  
LLENGUATGE [String()](../String().md)
