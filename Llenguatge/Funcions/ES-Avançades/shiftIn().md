---
títol: "shiftIn()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Avançades"
---

# shiftIn()

### Descripció

Canvia en un byte de dades un bit cada vegada. Comença des del bit més significatiu (és a dir, el més a l'esquerra) o menys (el més a la dreta). Per a cada bit, el pin del rellotge s'eleva, el següent bit es llig de la línia de dades i després el pin del rellotge es baixa.

Si està interactuant amb un dispositiu que té un rellotge amb flancs ascendents, haurà d'assegurar-se que el pin del rellotge estiga baix abans de la primera anomenada a `shiftIn()`, p.e. amb una anomenada a `digitalWrite(clockPin, LOW)`.

**Nota**: aquesta és una implementació de programari; Arduino també proporciona una [biblioteca SPI](https://www.arduino.cc/en/Reference/SPI) que utilitza la implementació de maquinari, que és més ràpida però només funciona en pins específics.

### Sintaxi

`byte incoming = shiftIn(dataPin, clockPin, bitOrder)`

### Paràmetres

`dataPin`: el pin en el qual ingressar cada bit. Tipus de dades permeses: int.  
`clockPin`: el pin per a alternar per a assenyalar una lectura de dataPin.  
`bitOrder`: quin ordre canviar en els bits; ja siga MSBFIRST o LSBFIRST. (Primer el bit més significatiu o Primer el bit menys significatiu).  

### Devolucions

El valor llegit. Tipus de dada: byte.

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
