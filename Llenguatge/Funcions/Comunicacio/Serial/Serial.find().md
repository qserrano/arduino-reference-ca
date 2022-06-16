---
títol: "Serial.find()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.find()

### Descripció

`Serial.find()` llig dades del búfer serial fins que es troba l'objectiu. La funció retorna vertader si es troba l'objectiu, fals si s'esgota el temps d'espera.

`Serial.find()` hereta de la classe d'utilitat [stream](../Stream.md).

### Sintaxi

`Serial.find(target)`  
`Serial.find(target, length)`

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal [Serial](../Serial.md).  
`target`: la cadena a buscar. Tipus de dades permeses: char.  
`length`: longitud de l'objectiu. Tipus de dades permeses: size_t.  

### Devolucions

Tipus de dada: booleà.

### Vegeu també

LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
