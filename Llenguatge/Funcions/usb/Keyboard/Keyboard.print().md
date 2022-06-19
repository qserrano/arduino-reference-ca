---
títol: "Keyboard.print()"
descripció: ""
categoria: "Funcions"
subcategoria: "Keyboard"
---

# Keyboard.print()

### Descripció

Envia una o més pulsacions de tecles a un ordinador connectat.

`Keyboard.print()` s'ha de cridar després d'iniciar `Keyboard.begin()`.

### Sintaxi

`Keyboard.print(character)`  
`Keyboard.print(characters)`  

### Paràmetres

`character`: un char o int que s'enviarà a l'ordinador com a tecla.  
`characters`: una cadena que s'enviarà a l'ordinador com a pulsacions de tecles.  

### Devolucions

Nombre de pulsacions de tecles enviades. Tipus de dades: size_t.

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

Quan utilitzeu l'ordre `Keyboard.print()`, l'Arduino es fa càrrec del vostre teclat! Assegureu-vos que teniu el control abans d'utilitzar l'ordre. Un polsador per canviar l'estat de control del teclat és efectiu.

### Veure també

LLENGUATGE [Keyboard](../Keyboard.md)  
LLENGUATGE [Funcions](../../../Funcions.md)  
