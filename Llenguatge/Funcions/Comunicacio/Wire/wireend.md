---
títol: "Wire.end()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Wire"
---

# end()

### Descripció

Deshabilita la biblioteca Wire, revertint l'efecte de `Wire.begin()`. Per a tornar a utilitzar la biblioteca Wire després d'això, torne a cridar a `Wire.begin()`.

**Nota**: aquesta funció no estava disponible en la versió original de la biblioteca Wire i és possible que encara no estiga disponible en totes les plataformes. El codi que ha de ser portàtil entre plataformes i versions pot usar la macro WIRE_HAS_END, que només es defineix quan `Wire.end()` està disponible.

### Sintaxi

`Wire.end()`

### Paràmetres

Cap.

### Devolucions

Cap.

### Vegeu també

LLENGUATGE [Wire](../wire.md)  
LLENGUATGE [Funcions](../../../Funcions.md)

