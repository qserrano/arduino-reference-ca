---
títol: "SPI.usingInterrupt()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "SPI"
---

# SPI.usingInterrupt()

### Descripció

Si el vostre programa realitzarà transaccions SPI dins d'una interrupció, truqueu a aquesta funció per registrar el número o el nom d'interrupció a la biblioteca SPI. Això permet a `SPI.beginTransaction()` evitar conflictes d'ús. Tingueu en compte que la interrupció especificada a la crida a `usingInterrupt()` es desactivarà en una trucada a `beginTransaction()` i es tornarà a habilitar a `endTransaction()`.

### Sintaxi

`SPI.usingInterrupt(interruptNumber)`  

### Paràmetres

`interruptNumber`: el número d'interrupció associat.  

### Devolucions

Cap.

### Vegeu també

LLENGUATGE [SPI](../spi.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
