
| títol | categoria  | subcategoria | subfunció |
| :---: | :--------: | :----------: | :-------: |
| Mouse.end() | Funcions | USB | Mouse |

# Mouse.end()

### Descripció

Deixa d'emular el ratolí connectat a un ordinador. Per iniciar el control, utilitzeu `Mouse.begin()`.

### Sintaxi

* `Mouse.end()`

### Paràmetres

* Cap

### Devolucions

Res

### Exemple de codi

```
#include <Mouse.h>

void setup() {
  pinMode(2, INPUT);
  //initiate the Mouse library
  Mouse.begin();
}

void loop() {
  //if the button is pressed, send a left mouse click
  //then end the Mouse emulation
  if (digitalRead(2) == HIGH) {
    Mouse.click();
    Mouse.end();
  }
}
```

### Vegeu també

* LLENGUATGE [Mouse](../Mouse.md)
