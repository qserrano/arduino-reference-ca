---
títol: "Keyboard.press()"
descripció: ""
categoria: "Funcions"
subcategoria: "Keyboard"
---

#Keyboard.press()

### Descripció

Quan es crida, `Keyboard.press()` funciona com si una tecla es prement i es mantingués al teclat. Útil quan s'utilitzen tecles modificadores. Per finalitzar la premsa de tecla, utilitzeu `Keyboard.release()` o `Keyboard.releaseAll()`.

Cal cridar a `Keyboard.begin()` abans d'utilitzar press().

### Sintaxi

`Keyboard.press(key)`

### Paràmetres

`key`: la tecla a prémer. Tipus de dades permesos: char.

### Devolucions

Nombre de pulsacions de tecles enviades. Tipus de dades: size_t.

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
  Keyboard.releaseAll();
  // wait for new window to open:
  delay(1000);
}
```
### Veure també

LLENGUATGE [Keyboard](../Keyboard.md)  
LLENGUATGE [Funcions](../../../Funcions.md)  
