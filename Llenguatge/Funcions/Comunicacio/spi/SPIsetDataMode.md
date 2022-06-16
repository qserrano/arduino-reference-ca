---
títol: "SPI.setDataMode"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "SPI"
---

# SPI.setDataMode()

### Descripció

Aquesta funció no s'ha d'utilitzar en projectes nous. Utilitzeu `SPISettings` amb `SPI.beginTransaction()`. per configurar els paràmetres SPI.

Estableix el mode de dades SPI: és a dir, la polaritat i la fase del rellotge. 

Consulteu l'article de la Viquipèdia sobre SPI per obtenir més informació.

### Sintaxi

`SPI.setDataMode (mode)`

### Paràmetres

`mode`:
* SPI_MODE0
* SPI_MODE1
* SPI_MODE2
* SPI_MODE3

`chipSelectPin`: pin CS del dispositiu perifèric (només Arduino Due)

### Devolucions

Cap.

### Vegeu també

LLENGUATGE [SPI](../spi.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
