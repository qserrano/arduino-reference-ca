---
títol: "reserve()"
categoria: [ "Variables" ]
subcategoria: [ "Tipus de dades" ]
subfunció: ["String()"]
---

# reserve()

## Descripció

La funció String reserve() us permet assignar un buffer a la memòria per manipular Strings.

## Sintaxi

`myString.reserve (size)`

## Paràmetres

`myString`: una variable de tipus String.  
`size`: el nombre de bytes a la memòria per guardar per a la manipulació de cadena. Tipus de dades permesos: unsigned int.

## Devolucions

Res

## Exemple de codi

```
String myString;

void setup() {
  // initialize serial and wait for port to open:
  Serial.begin(9600);
  while (!Serial) {
    ; // wait for serial port to connect. Needed for native USB
  }

  myString.reserve(26);
  myString = "i=";
  myString += "1234";
  myString += ", is that ok?";

  // print the String:
  Serial.println(myString);
}

void loop() {
  // nothing to do here
}
```

## Vegeu també

EXEMPLE [Tutorials de cadenes](https://www.arduino.cc/en/Tutorial/BuiltInExamples#strings) (en anglés)  
LLENGUATGE [String()](../String().md)
