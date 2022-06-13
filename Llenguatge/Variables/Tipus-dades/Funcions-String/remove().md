---
títol: "remove()"
categoria: [ "Variables" ]
subcategoria: [ "Tipus de dades" ]
subfunció: ["String()"]
---

# remove()

## Descripció

Modifica una cadena al seu lloc eliminant caràcters de l'índex proporcionat fins al final de la cadena o de l'índex proporcionat a l'índex més el recompte.

## Sintaxi

`myString.remove(index)`  
`myString.remove(índex, count)`

## Paràmetres

`myString`: una variable de tipus String  
`índex`: la posició en què s'inicia el procés d'eliminació (zero indexat). Tipus de dades permesos: int sense sign  
`count`: el nombre de caràcters que cal eliminar. Tipus de dades permesos: int sense sign.

## Devolucions

Res

## Exemple de codi

```
String salutacio = "hello";
salutacio.remove(2, 2); // salutacio ara conté "heo"
```

## Vegeu també

EXEMPLE [Tutorials de cadenes](https://www.arduino.cc/en/Tutorial/BuiltInExamples#strings) (en anglés)  
LLENGUATGE [String()](../String().md)
