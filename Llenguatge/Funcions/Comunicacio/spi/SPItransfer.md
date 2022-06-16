---
títol: "SPI.transfer()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "SPI"
---

# SPI.transfer()

### Descripció

La transferència SPI es basa en un enviament i una recepció simultània: les dades rebudes es retornen a receiveVal (o receiveVal16). En cas de transferències de memòria intermèdia, les dades rebudes s'emmagatzemen a la memòria intermèdia local (les dades antigues es substitueixen per les dades rebudes).

### Sintaxi

`rebutVal = SPI.transfer(val)`  
`rebutVal16 = SPI.transfer16(val16)`  
`SPI.transfer (búfer, mida)`  

### Paràmetres

`val`: el byte a enviar a través del bus  
`val16`: la variable de dos bytes per enviar a través del bus  
`buffer`: la matriu de dades a transferir  

### Devolucions

Les dades rebudes.

### Vegeu també

LLENGUATGE [SPI](../spi.md)  
LLENGUATGE [Funcions](../../Funcions.md)  
