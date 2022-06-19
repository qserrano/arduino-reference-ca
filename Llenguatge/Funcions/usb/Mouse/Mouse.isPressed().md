---
títol: "Mouse.isPressed()"
descripció: ""
categoria: "Funcions"
subcategoria: "USB"
funcio: "Mouse"
---

# Mouse.isPressed()

### Descripció

Comprova l'estat actual de tots els botons del ratolí i informa si se'n prem o no.

### Sintaxi

`Mouse.isPressed();`  
`Mouse.isPressed(button);`  

### Paràmetres

Quan no es passa cap valor, comprova l'estat del botó esquerre del ratolí.  
`button`: quin botó del ratolí cal comprovar. Tipus de dades permesos: char.
  - MOUSE_LEFT (predeterminat)
  - MOUSE_RIGHT
  - MOUSE_MIDDLE

### Devolucions

Informa si es prem un botó o no. Tipus de dades: bool.

### Exemple de codi

```
#include <Mouse.h>

void setup() {
  //The switch that will initiate the Mouse press
  pinMode(2, INPUT);
  //The switch that will terminate the Mouse press
  pinMode(3, INPUT);
  //Start serial communication with the computer
  Serial.begin(9600);
  //initiate the Mouse library
  Mouse.begin();
}

void loop() {
  //a variable for checking the button's state
  int mouseState = 0;
  //if the switch attached to pin 2 is closed, press and hold the left mouse button and save the state ina  variable
  if (digitalRead(2) == HIGH) {
    Mouse.press();
    mouseState = Mouse.isPressed();
  }
  //if the switch attached to pin 3 is closed, release the left mouse button and save the state in a variable
  if (digitalRead(3) == HIGH) {
    Mouse.release();
    mouseState = Mouse.isPressed();
  }
  //print out the current mouse button state
  Serial.println(mouseState);
  delay(10);
}
```

### Vegeu també

LLENGUATGE [Mouse](../Mouse.md)
