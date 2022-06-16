---
títol: "Serial.findUntil()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.findUntil()

### Descripció

`Serial.findUntil()` llig dades del búfer serial fins que es troba una cadena de destí de longitud donada o una cadena de terminació.

La funció retorna vertader si es troba la cadena de destí, fals si s'esgota el temps d'espera.

`Serial.findUntil()` hereta de la classe d'utilitat [stream](../Stream.md).

### Sintaxi

`Serial.findUntil(target, terminal)`

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal [Serial](../Serial.md).  
`target`: la cadena a buscar. Tipus de dades permeses: char.  
`terminal`: la cadena terminal en la cerca. Tipus de dades permeses: char.  

### Devolucions

Tipus de dada: booleà.

### Vegeu també

LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
