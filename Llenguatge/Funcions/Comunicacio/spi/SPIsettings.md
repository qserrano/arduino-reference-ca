---
títol: "SPIsettings"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "SPI"
---

# SPISettings

### Descripció

L'objecte SPISettings s'utilitza per configurar el port SPI del vostre dispositiu SPI. Els 3 paràmetres es combinen en un sol objecte SPISettings, que es dóna a `SPI.beginTransaction()`.

Quan tots els vostres paràmetres són constants, SPISettings s'ha d'utilitzar directament a `SPI.beginTransaction()`. Vegeu la secció de sintaxi a continuació. Per a les constants, aquesta sintaxi dóna com a resultat un codi més petit i més ràpid.

Si algun dels vostres paràmetres és variable, podeu crear un objecte SPISettings per contenir els 3 paràmetres. A continuació, podeu donar el nom de l'objecte a `SPI.beginTransaction()`. La creació d'un objecte SPISettings amb nom pot ser més eficient quan la vostra configuració no és constant, especialment si la velocitat màxima és una variable calculada o configurada, en lloc d'un número que escriviu directament al vostre croquis.

### Sintaxi

`SPI.beginTransaction(SPISettings(14000000, MSBFIRST, SPI_MODE0))` **Nota**: millor si els 3 paràmetres són constants  
`SPISettings mySetting(speedMaximum, dataOrder, dataMode)` **Nota**: Millor quan qualsevol paràmetre és una variable  

### Paràmetres

`speedMaximum`: la velocitat màxima de comunicació. Per a un xip SPI de fins a 20 MHz, utilitzeu 20000000.  
`DataOrder`: MSBFIRST o LSBFIRST  
`DataMode`: SPI_MODE0, SPI_MODE1, SPI_MODE2 o SPI_MODE3  

### Devolucions

Cap.

### Vegeu també

LLENGUATGE [SPI](../spi.md)
LLENGUATGE [Funcions](../../../Funcions.md)
