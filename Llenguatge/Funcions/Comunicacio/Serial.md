---
títol: "Serial"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
---

# Serial

### Descripció

S'utilitza per a la comunicació entre la placa Arduino i una computadora o altres dispositius. Totes les plaques Arduino tenen almenys un port serie (també conegut com UART o USART), i algunes tenen varis.

### Ports sèrie disponibles per cada placa

| Placa | Nom del USB CDC | Serial pins | Serial1 pins | Serial2 pins | Serial3 pins
| --- | --- | --- | --- | --- | ---
| Uno, Nano, Mini |  | 0(RX), 1(TX)
| Mega |  | 0(RX), 1(TX) | 19(RX), 18(TX) | 17(RX), 16(TX) | 15(RX), 14(TX)
| Leonardo, Micro, Yún | Serial |  | 0(RX), 1(TX)
| Uno WiFi Rev.2 |  | Connexió per USB | 0(RX), 1(TX) | Connexió a  NINA
| MKR boards | Serial |  | 13(RX), 14(TX)
| Zero | SerialUSB (només port USB nadiu) | Connexió a port de programació. | 0(RX), 1(TX)
| Due | SerialUSB (només port USB nadiu) | 0(RX), 1(TX) | 19(RX), 18(TX) | 17(RX), 16(TX) | 15(RX), 14(TX)
| 101 | Serial |  | 0(RX), 1(TX)

En UNO, Nano, Mini i Mega, els pins 0 i 1 s'utilitzen per a la comunicació amb la computadora. Connectar qualsevol cosa a aquests pins pot interferir amb aqueixa comunicació, fins i tot causar càrregues fallides a la placa.

Pot utilitzar el monitor serie integrat de l'entorn Arduino per a comunicar-se amb una placa Arduino. Faça clic en el botó del monitor serie en la barra d'eines i seleccione la mateixa velocitat en bauds utilitzada en la crida `begin()`.

La comunicació serial en els pins TX/RX usa nivells lògics TTL (5V o 3.3V depenent de la placa). No connecte aquests pins directament a un port serie RS232; funcionen a +/- 12V i poden danyar la seua placa Arduino.

Per a usar aquests ports sèrie addicionals per a comunicar-se amb la seua computadora personal, necessitarà un adaptador USB a sèrie addicional, ja que no estan connectats a l'adaptador USB a sèrie del Mega. Per a usar-los per a comunicar-se amb un dispositiu serial TTL extern, connecte el pin TX al pin RX del seu dispositiu, el RX al pin TX del seu dispositiu i la terra del seu Mega a la terra del seu dispositiu.

### Funcions

- [if(Serial)](./Serial/if(Serial).md)
- [available()](./Serial/Serial.available().md)
- [availableForWrite()](./Serial/Serial.availableForWrite().md)
- [begin()](./Serial/Serial.begin().md)
- [end()](./Serial/Serial.end().md)
- [find()](./Serial/Serial.find().md)
- [findUntil()](./Serial/Serial.findUntil().md)
- [flush()](./Serial/Serial.flush().md)
- [parseFloat()](./Serial/Serial.parseFloat().md)
- [parseInt()](./Serial/Serial.parseInt().md)
- [peek()](./Serial/Serial.peek().md)
- [print()](./Serial/Serial.print().md)
- [println()](./Serial/Serial.println().md)
- [read()](./Serial/Serial.read().md)
- [readBytes()](./Serial/Serial.readBytes().md)
- [readBytesUntil()](./Serial/Serial.readBytesUntil().md)
- [readString()](./Serial/Serial.readString().md)
- [readStringUntil()](./Serial/Serial.readStringUntil().md)
- [setTimeout()](./Serial/Serial.setTimeout().md)
- [write()](./Serial/Serial.write().md)
- [serialEvent()](./Serial/Serial.serialEvent().md)
