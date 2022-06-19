---
títol: "Keyboard.end()"
descripció: ""
categoria: "Funcions"
subcategoria: "Keyboard"
---

# Keyboard.end()

### Descripció

Atura l'emulació del teclat a un ordinador connectat. Per iniciar l'emulació del teclat, utilitzeu `Keyboard.begin().`

### Sintaxi

`Keyboard.end()`

### Paràmetres

Cap

### Devolucions

Res

### Exemple de codi

```
#include <Keyboard.h>

void setup() {
  //start keyboard communication
  Keyboard.begin();
  //send a keystroke
  Keyboard.print("Hello!");
  //end keyboard communication
  Keyboard.end();
}

void loop() {
  //do nothing
}
```
### Veure també

LLENGUATGE [Keyboard](../Keyboard.md)  
LLENGUATGE [Funcions](../../../Funcions.md)  
