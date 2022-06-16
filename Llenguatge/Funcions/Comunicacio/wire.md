---
títol: "Wire"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
---


# Wire

### Descripció

Esta biblioteca li permet comunicar-se amb dispositius I2C/TWI. En les plaques Arduino amb el disseny R3 (pinout 1.0), SDA (línia de dades) i SCL (línia de rellotge) estan en els encapçalats dels pins a prop del pin AREF. El Arduino Dues té dues interfícies I2C/TWI SDA1 i SCL1 que estan a prop del pin AREF i l'addicional està en els pins 20 i 21.

Com a referència, la següent taula mostra on es troben els pins TWI en diverses plaques Arduino.

| Placa | pins I2C/TWI |
| ----- | ------------ |
| UNO, Ethernet | A4 (SDA), A5 (SCL) |
| Mega2560      | 20 (SDA), 21 (SCL) |
| leonardo      | 20 (SDA), 21 (SCL), SDA1, SCL1 |

A partir d'Arduino 1.0, la biblioteca hereta de les funcions Stream, cosa que la fa coherent amb altres biblioteques de lectura/escriptura. A causa d'això, enviar() i rebre() han estat reemplaçats per llegir() i escriure().


Les versions recents de la biblioteca Wire poden utilitzar temps d'espera per evitar un bloqueig davant de certs problemes al bus, però això no està habilitat per defecte (encara) a les versions actuals. Es recomana habilitar sempre aquests temps d'espera en fer servir la biblioteca Wire. Consulteu la funció Wire.setWireTimeout per obtenir més detalls.

**Nota**: Hi ha versions de 7 i 8 bits d'adreces I2C. 7 bits identifiquen el dispositiu, i el vuitè bit determina si s'està escrivint o llegint. La biblioteca Wire utilitza adreces de 7 bits en tot moment. Si teniu un full de dades o un codi de mostra que utilitza una adreça de 8 bits, voldreu eliminar el bit baix (és a dir, canviar el valor un bit a la dreta), la qual cosa genera una adreça entre 0 i 127. No obstant això. , les adreces de 0 a 7 no es fan servir perquè estan reservats, de manera que la primera adreça que es pot usar és 8. Tingueu en compte que es necessita una resistència pull-up quan es connecten els pins SDA/SCL. Consulteu els exemples per obtenir més informació. La placa MEGA 2560 té resistències pull-up als pins 20 i 21 integrats.

La implementació de la biblioteca Wire utilitza un memòria intermèdia de 32 bytes, per la qual cosa qualsevol comunicació ha d'estar dins aquest límit. Els bytes en excés en una sola transmissió simplement s'eliminaran.

### Sintaxi

* `#include <Wire.h>`

### Funcions

* [begin()](./Wire/wirebegin.md)
* [end()](./Wire/wireend.md)
* [requestFrom()](./Wire/wirerequestFrom.md)
* [beginTransmission()](./Wire/wirebeginTransmission.md)
* [write()](./Wire/wirewrite.md)
* [available()](./wire/wireavailable.md)
* [read()](./wire/wireread.md)
* [setClock()](./Wire/wiresetClock.md)
* [onReceive()](./Wire/wireonReceive.md)
* [onRequest()](./Wire/wireonRequest.md)
* [setWireTimeout()](./Wire/wiresetWireTimeout.md)
* [clearWireTimeoutFlag()](./Wire/wireclearWireTimeoutFlag.md)
* [getWireTimeoutFlag()](./Wire/wiregetWireTimeoutFlag.md)
