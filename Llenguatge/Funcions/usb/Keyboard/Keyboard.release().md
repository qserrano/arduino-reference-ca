---
títol: "Keyboard.release()"
descripció: ""
categoria: "Funcions"
subcategoria: "Keyboard"
---

# Keyboard.release()

### Descripció

Allibera la tecla especificada. Vegeu `Keyboard.press()` per obtenir més informació.

### Sintaxi

`Keyboard.release (key)`

### Paràmetres

`key`: la tecla per alliberar. Tipus de dades permesos: char.

### Devolucions

El nombre de tecles alliberades. Tipus de dades: size_t.

### Exemple de codi

```
#include <Keyboard.h>

// use this option for OSX:
char ctrlKey = KEY_LEFT_GUI;
// use this option for Windows and Linux:
//  char ctrlKey = KEY_LEFT_CTRL;

void setup() {
  // make pin 2 an input and turn on the
  // pullup resistor so it goes high unless
  // connected to ground:
  pinMode(2, INPUT_PULLUP);
  // initialize control over the keyboard:
  Keyboard.begin();
}

void loop() {
  while (digitalRead(2) == HIGH) {
    // do nothing until pin 2 goes low
    delay(500);
  }
  delay(1000);
  // new document:
  Keyboard.press(ctrlKey);
  Keyboard.press('n');
  delay(100);
  Keyboard.release(ctrlKey);
  Keyboard.release('n');
  // wait for new window to open:
  delay(1000);
}
```

### Veure també

LLENGUATGE [Keyboard](../Keyboard.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
