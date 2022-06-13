
| títol | categoria  | subcategoria | subfunció |
| :---: | :--------: | :----------: | :-------: |
| Mouse.click() | Funcions | USB | Mouse |

# Mouse.click()

### Descripció

Envia un clic momentània a l'ordinador a la ubicació del cursor. Això és el mateix que prémer i deixar anar immediatament el botó del ratolí.

`Mouse.click()` és el botó esquerre del ratolí per defecte.

### Sintaxi

* `Mouse.click()`
* `Mouse.click(button)`

### Paràmetres

* `button`: quin botó del ratolí cal prémer. Tipus de dades permesos: char.
  - MOUSE_LEFT (predeterminat)
  - MOUSE_RIGHT
  - MOUSE_MIDDLE

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
  if (digitalRead(2) == HIGH) {
    Mouse.click();
  }
}
```

### Notes i advertències

Quan utilitzeu l'ordre Mouse.click(), l'Arduino es fa càrrec del vostre ratolí! Assegureu-vos que teniu el control abans d'utilitzar l'ordre. Un polsador per canviar l'estat de control del ratolí és efectiu.

### Vegeu també

* LLENGUATGE [Mouse](../Mouse.md)
