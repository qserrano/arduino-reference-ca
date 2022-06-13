
| títol | descripció   | categoria  | subcategoria        |
| :---: | :----------: | :--------: | :-----------------: |
| SPI.setBitOrder() | | Funcions | Comunicació |

# SPI.setBitOrder()

### Descripció

Aquesta funció no s'ha d'utilitzar en projectes nous. Utilitzeu SPISettings. amb SPI.beginTransaction(). per configurar els paràmetres SPI.

Estableix l'ordre dels bits desplaçats cap a fora i cap al bus SPI, ja sigui LSBFIRST (primer el bit menys significatiu) o MSBFIRST (primer el bit més significatiu).

### Sintaxi

* `SPI.setBitOrder(ordre)`

### Paràmetres

* `ordre`: LSBFIRST o MSBFIRST

### Devolucions

Cap.

### Vegeu també

*  LLENGUATGE [SPI](../spi.md)
*  LLENGUATGE [Funcions](../../Funcions.md)
