---
títol: "Wire.setClock()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Wire"
---

# setClock()

### Descripció

Aquesta funció modifica la freqüència de rellotge per a la comunicació I2C. Els dispositius perifèrics I2C no tenen una freqüència mínima de rellotge de treball, però 100 KHz sol ser la línia de base.

### Sintaxi

`Wire.setClock`(freqüència del rellotge)

### Paràmetres

`clockFrequency`: el valor (en Hertz) del rellotge de comunicació desitjat. Els valors acceptats són 100000 (mode estàndard) i 400000 (mode ràpid). Alguns processadors també admeten 10000 (mode de baixa velocitat), 1000000 (mode ràpid plus) i 3400000 (mode d'alta velocitat). Consulteu la documentació específica del processador per assegurar-vos que el mode desitjat és compatible.

### Devolucions

Cap.

### Vegeu també

LLENGUATGE [Wire](../wire.md)  
LLENGUATGE [Funcions](../../../Funcions.md)

