---
títol: "Wire.clearWireTimeoutFlag()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Wire"
---

# clearWireTimeoutFlag()

### Descripció

Esborra la marca del temps d'espera.

És possible que els temps d'espera no estiguin activats de manera predeterminada. Consulteu la documentació de `Wire.setWireTimeout()` per obtenir més informació sobre com configurar els temps d'espera i com funcionen.

### Sintaxi

`Wire.clearTimeout()`  

### Paràmetres

Cap.

### Devolucions

bool: el valor actual de la bandera

### Notes de portabilitat

Aquesta funció no estava disponible a la versió original de la biblioteca Wire i és possible que encara no estigui disponible a totes les plataformes. El codi que ha de ser portàtil entre plataformes i versions pot utilitzar la macro WIRE_HAS_TIMEOUT, que només es defineix quan `Wire.setWireTimeout()`, `Wire.getWireTimeoutFlag()` i `Wire.clearWireTimeout()` estan disponibles.

### Vegeu també

LLENGUATGE [Wire](../wire.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
