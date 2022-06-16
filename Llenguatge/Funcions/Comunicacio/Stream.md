---
títol: "Stream"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
---

# Stream

### Descripció

Stream és la classe base per a fluxos basats en caràcters i binaris. No es crida directament, sinó que s'invoca sempre que utilitzeu una funció que depèn d'ella.

Stream defineix les funcions de lectura a Arduino. Quan utilitzeu qualsevol funcionalitat bàsica que utilitzi un mètode `read()` o similar, podeu suposar amb seguretat que crida a la classe Stream. Per a funcions com `print()`, Stream hereta de la classe Print.

Algunes de les biblioteques que depenen de Stream inclouen: (enllaç al document en anglés)

- [Serial](https://www.arduino.cc/reference/en/language/functions/communication/serial)
- [Wire](https://www.arduino.cc/en/Reference/Wire)
- [Ethernet](https://www.arduino.cc/en/Reference/Ethernet)
- [SD](https://www.arduino.cc/en/Reference/SD)

Funcions

- [available()](./Stream/Stream.available().md)
- [read()](./Stream/Stream.read().md)
- [flush()](./Stream/Stream.flush().md)
- [find()](./Stream/Stream.find().md)
- [findUntil()](./Stream/Stream.findUntil().md)
- [peek()](./Stream/Stream.peek().md)
- [readBytes()](./Stream/Stream.readBytes().md)
- [readBytesUntil()](./Stream/Stream.readBytesUntil().md)
- [readString()](./Stream/Stream.readString().md)
- [readStringUntil()](./Stream/Stream.readStringUntil().md)
- [parseInt()](./Stream/Stream.parseInt().md)
- [parseFloat()](./Stream/Stream.parseFloat().md)
- [setTimeout()](./Stream/Stream.setTimeout().md)
