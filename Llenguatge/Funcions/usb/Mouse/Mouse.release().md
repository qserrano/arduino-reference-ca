
| títol | categoria  | subcategoria | subfunció |
| :---: | :--------: | :----------: | :-------: |
| Mouse.release() | Funcions | USB | Mouse |

# Mouse.release()

### Descripció

Envia un missatge que s'allibera un botó premut prèviament (invocat mitjançant `Mouse.press()`).

`Mouse.release()` és el botó esquerre per defecte.

### Sintaxi

* `Mouse.release()`
* `Mouse.release (button)`

### Paràmetres

* `button`: quin botó del ratolí cal prémer. Tipus de dades permesos: char.
  - MOUSE_LEFT (predeterminat)
  - MOUSE_REIGHT
  - MOUSE_MIDDLE

### Devolucions

Res

### Exemple de codi

```
#include <Mouse.h>

void setup() {
  //The switch that will initiate the Mouse press
  pinMode(2, INPUT);
  //The switch that will terminate the Mouse press
  pinMode(3, INPUT);
  //initiate the Mouse library
  Mouse.begin();
}

void loop() {
  //if the switch attached to pin 2 is closed, press and hold the left mouse button
  if (digitalRead(2) == HIGH) {
    Mouse.press();
  }
  //if the switch attached to pin 3 is closed, release the left mouse button
  if (digitalRead(3) == HIGH) {
    Mouse.release();
  }
}
```

### Notes i advertències

Quan utilitzeu l'ordre `Mouse.release()`, l'Arduino es fa càrrec del vostre ratolí! Assegureu-vos que teniu el control abans d'utilitzar l'ordre. Un polsador per canviar l'estat de control del ratolí és efectiu.

### Vegeu també

* LLENGUATGE [Mouse](../Mouse.md)
