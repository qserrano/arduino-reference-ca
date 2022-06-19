---
títol: "Mouse.press()"
descripció: ""
categoria: "Funcions"
subcategoria: "USB"
funcio: "Mouse"
---

# Mouse.press()

### Descripció

Envia un botó premut a un ordinador connectat. Un botó premut és l'equivalent a fer clic i mantenir premut el botó del ratolí. Es cancel·la amb `Mouse.release()`.

Abans d'utilitzar `Mouse.press()`, heu d'iniciar la comunicació amb `Mouse.begin()`.

`Mouse.press()` per defecte és una pressió del botó esquerre.

### Sintaxi

`Mouse.press()`  
`Mouse.press(button)`  

### Paràmetres

`botó`: quin botó del ratolí cal prémer. Tipus de dades permesos: char.  
  - MOUSE_LEFT (predeterminat)
  - MOUSE_RIGHT
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

Quan utilitzeu l'ordre `Mouse.press()`, l'Arduino es fa càrrec del vostre ratolí! Assegureu-vos que teniu el control abans d'utilitzar l'ordre. Un polsador per canviar l'estat de control del ratolí és efectiu.

### Vegeu també

LLENGUATGE [Mouse](../Mouse.md)
