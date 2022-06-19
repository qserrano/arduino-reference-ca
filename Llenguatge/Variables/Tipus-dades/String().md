---
títol: "String()"
categories: [ "Variables" ]
subcategories: [ "Tipus de dades" ]
---

# String()

## Descripció

Construeix una instància de la classe String. Hi ha diverses versions que construeixen cadenes a partir de diferents tipus de dades (és a dir, formatar-les com a seqüències de caràcters), com ara:

- una cadena constant de caràcters, entre cometes dobles (és a dir, una matriu de caràcters)
- un sol caràcter constant, entre cometes simples
- una altra instància de l'objecte String
- un nombre enter constant o un nombre enter llarg
- un nombre enter constant o un nombre enter llarg, utilitzant una base especificada
- una variable entera o entera llarga
- una variable entera o llarga, utilitzant una base especificada
- un flotant o doble, utilitzant una xifra decimal especificada

La construcció d'una cadena a partir d'un nombre dóna com a resultat una cadena que conté la representació ASCII d'aquest nombre. El valor predeterminat és la base deu, per tant

`String thisString = String(13);`

us dóna la cadena "13". Tanmateix, podeu utilitzar altres bases. Per exemple,

`String thisString = String(13, HEX);`

us dóna la cadena "d", que és la representació hexadecimal del valor decimal 13. O si preferiu el binari,

`String thisString = String(13, BIN);`

us dóna la cadena "1101", que és la representació binària de 13.

## Sintaxi

`String (val)`  
`String (val, base)`  
`String (val, decimalPlaces)`

## Paràmetres

`val`: una variable per formatar com a cadena. Tipus de dades permesos: string, char, byte, int, long, unsigned int, unsigned long, float, double.  
`base`: (opcional) la base en què formatar un valor integral.  
`decimalPlaces`: només si val és float o double. Les xifres decimals desitjades.

## Devolucions

Una instància de la classe String.

## Exemple de codi

Totes les següents són declaracions vàlides per a Strings.

```
String stringOne = "Hello String";                    // using a constant String
String stringOne = String('a');                       // converting a constant char into a String
String stringTwo = String("This is a string");        // converting a constant string into a String object
String stringOne = String(stringTwo + " with more");  // concatenating two strings
String stringOne = String(13);                        // using a constant integer
String stringOne = String(analogRead(0), DEC);        // using an int and a base
String stringOne = String(45, HEX);                   // using an int and a base (hexadecimal)
String stringOne = String(255, BIN);                  // using an int and a base (binary)
String stringOne = String(millis(), DEC);             // using a long and a base
String stringOne = String(5.698, 3);                  // using a float and the decimal places
```

## Funcions

- [charAt()](./Funcions-String/charAt().md)
- [compareTo()](./Funcions-String/compareTo().md)
- [concat()](./Funcions-String/concat().md)
- [c_str()](./Funcions-String/c_str().md)
- [endsWith()](./Funcions-String/endsWith().md)
- [equals()](./Funcions-String/equals().md)
- [equalsIgnoreCase()](./Funcions-String/equalsIgnoreCase().md)
- [getBytes()](./Funcions-String/getBytes().md)
- [indexOf()](./Funcions-String/indexOf().md)
- [lastIndexOf()](./Funcions-String/lastIndexOf().md)
- [length()](./Funcions-String/length().md)
- [remove()](./Funcions-String/remove().md)
- [replace()](./Funcions-String/replace().md)
- [reserve()](./Funcions-String/reserve().md)
- [setCharAt()](./Funcions-String/setCharAt().md)
- [startsWith()](./Funcions-String/startsWith().md)
- [substring()](./Funcions-String/substring().md)
- [toCharArray()](./Funcions-String/toCharArray().md)
- [toDouble()](./Funcions-String/toDouble().md)
- [toInt()](./Funcions-String/toInt().md)
- [toFloat()](./Funcions-String/toFloat().md)
- [toLowerCase()](./Funcions-String/toLowerCase().md)
- [toUpperCase()](./Funcions-String/toUpperCase().md)
- [trim()](./Funcions-String/trim().md)

## Operadors

- [] [(element access)](./Operadors/element_access.md)
- \+ [(concatenation)](./Operadors/concatenation.md)
- += [(append)](./Operadors/append.md)
- == [(comparison)](./Operadors/comparison.md)
- \> [(greater than)](./Operadors/greater_than.md)
- \>= [(greater than or equal to)](./Operadors/greater_than_or_equal_to.md)
- < [(less than)](./Operadors/less_than.md)
- <= [(less than or equal to)](./Operadors/less_than_or_equal_to.md)
- != [(different from)](./Operadors/different_from.md)
- [String Tutorials](https://www.arduino.cc/en/Tutorial/BuiltInExamples#strings)

## Veure també

LLENGUATGE [Variables](../../Variables.md)
