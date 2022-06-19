---
títol: "Mouse"
descripció: ""
categoria: "Funcions"
subcategoria: "USB"
---

# Mouse

### Descripció

Les funcions del ratolí permeten que les plaques basades en micro 32u4 o SAMD controlin el moviment del cursor en un ordinador connectat mitjançant el port USB natiu del seu micro. Quan actualitzeu la posició del cursor, sempre és relativa a la ubicació anterior del cursor.

### Notes i advertències

Aquestes biblioteques bàsiques permeten que les plaques basades en 32u4 i SAMD (Leonardo, Esplora, Zero, Due i MKR Family) apareguin com a ratolí i/o teclat nadius a un ordinador connectat.

Una precaució sobre l'ús de les biblioteques del ratolí i del teclat: si la biblioteca del ratolí o del teclat s'està executant constantment, serà difícil programar el vostre tauler. Funcions com `Mouse.move()` i `Keyboard.print()` mouran el cursor o enviaran pulsacions de tecles a un ordinador connectat i només s'han de cridar quan estigueu preparats per gestionar-les. Es recomana utilitzar un sistema de control per activar aquesta funcionalitat, com ara un interruptor físic o només responent a una entrada específica que podeu controlar. Consulteu els exemples de ratolí i teclat per obtenir algunes maneres de gestionar-ho.

Quan utilitzeu la biblioteca del ratolí o del teclat, potser és millor provar la vostra sortida primer amb `Serial.print()`. D'aquesta manera, podeu estar segur de saber quins valors s'estan informant.

### Funcions

- [Mouse.begin()](./Mouse/Mouse.begin().md)
- [Mouse.click()](./Mouse/Mouse.click().md)
- [Mouse.end()](./Mouse/Mouse.end().md)
- [Mouse.move()](./Mouse/Mouse.move().md)
- [Mouse.press()](./Mouse/Mouse.press().md)
- [Mouse.release()](./Mouse/Mouse.release().md)
- [Mouse.isPressed()](./Mouse/Mouse.isPressed().md)

### Vegeu també (en anglés)

- EXEMPLE [KeyboardAndMouseControl](http://www.arduino.cc/en/Tutorial/KeyboardAndMouseControl): demostra les ordres del ratolí i del teclat en un sol programa.
- EXEMPLE [ButtonMouseControl](http://www.arduino.cc/en/Tutorial/ButtonMouseControl): Controla el moviment del cursor amb 5 polsadors.
- EXEMPLE [JoystickMouseControl](http://www.arduino.cc/en/Tutorial/JoystickMouseControl): controla el moviment del cursor d'un ordinador amb un joystick quan es prem un botó.

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
