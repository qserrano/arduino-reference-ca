---
títol: "detachInterrupt()"
descripció: ""
categoria: "Funcions"
subcategoria: "Interrupcions externes"
---

# detachInterrupt()

### Descripció

Desactiva la interrupció donada.

### Sintaxi

`detachInterrupt(digitalPinToInterrupt(pin))` (recomanat)  
`detachInterrupt(interrupció)` (no recomanat)  
`detachInterrupt(pin)` (no recomanat. A més, aquesta sintaxi només funciona amb plaques Arduino SAMD, Uno WiFi Rev2, Due i 101.)

### Paràmetres

`interrupció`: el número de la interrupció a desactivar (vegeu attachInterrupt() per a més detalls).  
`pin` el número de pin Arduino de la interrupció per desactivar

### Devolucions

Res

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
