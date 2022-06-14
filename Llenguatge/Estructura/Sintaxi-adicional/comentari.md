---
títol: "//"
descripció: "comentari"
categoria: "Estructura"
subcategoria: "Sintaxi adicional"
---

# //

### Descripció

Els comentaris són línies en el programa que s'utilitzen per a informar-se a si mateix o a altres sobre la forma en què funciona el programa. El compilador els ignora i no els exporta al processador, per la qual cosa no ocupen espai en la memòria flaix del microcontrolador. L'únic propòsit dels comentaris és ajudar-lo a comprendre (o recordar) o informar a uns altres sobre com funciona el seu programa.

Un comentari d'una sola línia comença amb // (dues barres inclinades adjacents). Aquest comentari acaba automàticament al final d'una línia. El que seguisca // fins al final d'una línia serà ignorat pel compilador.

### Codi d'exemple

Hi ha dues formes diferents de marcar una línia com a comentari:

```
// el pin 13 té un LED connectat en la majoria de les plaques Arduino.
// Dona-li un nom:
int led = 13;
digitalWrite(led, HIGH); // encén el LED (HIGH és el nivell alt de voltatge)
```

### Notes i Advertiments

En experimentar amb el codi, "comentar" parts del seu programa és una forma convenient d'eliminar línies que poden tindre errors. Això deixa les línies en el codi, però les converteix en comentaris, per la qual cosa el compilador les ignora. Això pot ser especialment útil quan es tracta de localitzar un problema o quan un programa es nega a compilar i l'error del compilador és críptic o inútil.

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)  
