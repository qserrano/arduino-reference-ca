---
títol: "toFloat()"
categoria: [ "Variables" ]
subcategoria: [ "Tipus de dades" ]
subfunció: ["String()"]
---

# toFloat()

## Descripció

Converteix una cadena vàlida en flotant. La cadena d'entrada hauria de començar amb un dígit. Si la cadena conté caràcters que no són dígits, la funció deixarà de realitzar la conversió. Per exemple, les cadenes "123.45", "123" i "123fish" es converteixen a 123.45, 123.00 i 123.00 respectivament. Tingueu en compte que "123.456" s'aproxima a 123.46. Tingueu en compte també que els flotants només tenen de 6 a 7 dígits decimals de precisió i que les cadenes més llargues es poden truncar.

## Sintaxi

`myString.toFloat()`

## Paràmetres

`myString`: una variable de tipus String

## Devolucions

Si no es pot realitzar cap conversió vàlida perquè la cadena no comença amb un dígit, es retorna un zero. Tipus de dades: flotant

## Vegeu també

EXEMPLE [Tutorials de cadenes](https://www.arduino.cc/en/Tutorial/BuiltInExamples#strings) (en anglés)  
LLENGUATGE [String()](../String().md)
