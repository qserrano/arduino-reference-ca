---
títol: "Keyboard"
descripció: ""
categoria: "Funcions"
subcategoria: "USB"
---

# Keyboard

### Descripció

Les funcions del teclat permeten que les plaques basades en micro 32u4 o SAMD enviïn pulsacions de tecles a un ordinador connectat a través del port USB natiu del seu micro.

Nota: No tots els caràcters ASCII possibles, especialment els que no s'imprimeixen, es poden enviar amb la biblioteca del teclat.

La biblioteca admet l'ús de tecles modificadores. Les tecles modificadores canvien el comportament d'una altra tecla quan es prem simultàniament. [Vegeu aquí](https://www.arduino.cc/reference/en/language/functions/usb/keyboard/keyboardmodifiers) (en anglés) per obtenir informació addicional sobre les claus admeses i el seu ús.

### Notes i advertències

Aquestes biblioteques bàsiques permeten que les plaques basades en 32u4 i SAMD (Leonardo, Esplora, Zero, Due i MKR Family) apareguin com a ratolí i/o teclat nadius a un ordinador connectat.

**Una precaució sobre l'ús de les biblioteques del ratolí i del teclat**: si la biblioteca del ratolí o del teclat s'està executant constantment, serà difícil programar la vostra placa. Funcions com `Mouse.move()` i `Keyboard.print()` mouran el cursor o enviaran pulsacions de tecles a un ordinador connectat i només s'han de cridar quan estigueu preparats per gestionar-les. Es recomana utilitzar un sistema de control per activar aquesta funcionalitat, com ara un interruptor físic o només responent a una entrada específica que podeu controlar. Consulteu els exemples de ratolí i teclat per obtenir algunes maneres de gestionar-ho.

Quan utilitzeu la biblioteca del ratolí o del teclat, potser és millor provar la vostra sortida primer amb `Serial.print()`. D'aquesta manera, podeu estar segur de saber quins valors s'estan informant.

Funcions

- [Keyboard.begin()](./Keyboard/Keyboard.begin().md)
- [Keyboard.end()](./Keyboard/Keyboard.end().md)
- [Keyboard.press()](./Keyboard/Keyboard.press().md)
- [Keyboard.print()](./Keyboard/Keyboard.print().md)
- [Keyboard.println()](./Keyboard/Keyboard.println().md)
- [Keyboard.release()](./Keyboard/Keyboard.release().md)
- [Keyboard.releaseAll()](./Keyboard/Keyboard.releaseAll().md)
- [Keyboard.write()](./Keyboard/Keyboard.write().md)

### Vegeu també (en anglés)

* EXEMPLE [KeyboardAndMouseControl](http://www.arduino.cc/en/Tutorial/KeyboardAndMouseControl): demostra les ordres del ratolí i del teclat en un sol programa.
* EXEMPLE [KeyboardLogout](http://www.arduino.cc/en/Tutorial/KeyboardLogout): tanca la sessió de l'usuari actual amb les ordres de tecla
* EXEMPLE [KeyboardSerial](http://www.arduino.cc/en/Tutorial/KeyboardSerial): llegeix un byte del port sèrie i envia de nou una pulsació de tecla.
* EXEMPLE [KeyboardReprogram](http://www.arduino.cc/en/Tutorial/KeyboardReprogram): obre una finestra nova a l'IDE d'Arduino i reprograma la placa amb un simple programa de parpelleig

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
