---
títol: "Wire.getWireTimeoutFlag()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Wire"
---

# getWireTimeoutFlag()

### Descripció

Comprova si s'ha produït un temps d'espera des de l'última vegada que es va esborrar el senyalador.

Aquest indicador s'estableix quan es produeix un temps d'espera i s'esborra quan es crida a Wire.clearWireTimeoutFlag() o quan es canvia el temps d'espera mitjançant `Wire.setWireTimeout()`.

### Sintaxi

`Wire.getWireTimeoutFlag()`

### Paràmetres

Cap.

### Devolucions

bool: el valor actual de la bandera

### Notes de portabilitat

Aquesta funció no estava disponible a la versió original de la biblioteca Wire i és possible que encara no estigui disponible a totes les plataformes. El codi que ha de ser portàtil entre plataformes i versions pot utilitzar la macro WIRE_HAS_TIMEOUT, que només es defineix quan `Wire.setWireTimeout()`, `Wire.getWireTimeoutFlag()` i `Wire.clearWireTimeout()` estan disponibles.

### Vegeu també

LLENGUATGE [Wire](../wire.md)  
LLENGUATGE [Funcions](../../Funcions.md)
