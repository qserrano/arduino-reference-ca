---
títol: "Keyboard.begin()"
descripció: ""
categoria: "Funcions"
subcategoria: "Keyboard"
---

# Keyboard.begin()

### Descripció

Quan s'utilitza amb una placa Leonardo o Due, `Keyboard.begin()` comença a emular un teclat connectat a un ordinador. Per finalitzar el control, utilitzeu `Keyboard.end()`.

### Sintaxi

`Keyboard.begin()`  
`Keyboard.begin (layout)`  

### Paràmetres

`layout`: la disposició del teclat a utilitzar. Aquest paràmetre és opcional i el valor predeterminat és KeyboardLayout_en_US.

### Disposicions del teclat

Actualment, la biblioteca admet els següents dissenys de teclat nacionals:
- KeyboardLayout_de_DE: Alemanya
- KeyboardLayout_en_US: EUA
- KeyboardLayout_es_ES: Espanya
- KeyboardLayout_fr_FR: França
- KeyboardLayout_it_IT: Itàlia

### Devolucions

Res

### Exemple de codi

```
#include <Keyboard.h>

void setup() {
  // make pin 2 an input and turn on the
  // pullup resistor so it goes high unless
  // connected to ground:
  pinMode(2, INPUT_PULLUP);
  Keyboard.begin();
}

void loop() {
  //if the button is pressed
  if (digitalRead(2) == LOW) {
    //Send the message
    Keyboard.print("Hello!");
  }
}
```

### Notes i advertències

Es poden crear dissenys personalitzats copiant i modificant un disseny existent. Consulteu les instruccions al fitxer KeyboardLayout.h de la biblioteca del teclat.

### Veure també

LLENGUATGE [Keyboard](../Keyboard.md)  
LLENGUATGE [Funcions](../../../Funcions.md)  
