---
títol: "Keyboard.write()"
descripció: ""
categoria: "Funcions"
subcategoria: "Keyboard"
---

# Keyboard.write()

### Descripció

Envia una pulsació de tecla a un ordinador connectat. Això és similar a prémer i deixar anar una tecla del teclat. Podeu enviar alguns caràcters ASCII o modificadors de teclat addicionals i tecles especials.

Només s'admeten els caràcters ASCII que es troben al teclat. Per exemple, ASCII 8 (backspace) funcionaria, però ASCII 25 (substitució) no. Quan s'envia lletres majúscules, Keyboard.write() envia una ordre de majúscules més el caràcter desitjat, tal com si escrivia amb un teclat. Si s'envia un tipus numèric, l'envia com a caràcter ASCII (p. ex. Keyboard.write(97) enviarà 'a').

Per obtenir una llista completa de caràcters ASCII, consulteu [ASCIITable.com](http://www.asciitable.com/).

### Sintaxi

`Keyboard.write (character)`

### Paràmetres

`character`: un char o int que s'enviarà a l'ordinador. Es pot enviar amb qualsevol notació que sigui acceptable per a un char. Per exemple, tots els següents són acceptables i envien el mateix valor, 65 o ASCII A:
  - Keyboard.write(65); // envia el valor ASCII 65, o A
  - Keyboard.write('A'); // el mateix que un caràcter citat
  - Keyboard.write(0x41); // el mateix en hexadecimal
  - Keyboard.write(0b01000001); // el mateix en binari (elecció estranya, però funciona)

### Devolucions

Nombre de bytes enviats. Tipus de dades: size_t.

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
    //Send an ASCII 'A',
    Keyboard.write(65);
  }
}
```

### Notes i advertències

Quan utilitzeu l'ordre `Keyboard.write()`, l'Arduino es fa càrrec del vostre teclat! Assegureu-vos que teniu el control abans d'utilitzar l'ordre. Un polsador per canviar l'estat de control del teclat és efectiu.

### Veure també

LLENGUATGE [Keyboard](../Keyboard.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
