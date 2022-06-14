---
títol: "%="
descripció: "mòdul compost"
categoria: "Estructura"
subcategoria: "Operadors compostos"
---

# %=

### Descripció

Aquesta és una abreviatura convenient per calcular la resta quan es divideix un nombre enter per un altre i tornar-lo a assignar a la variable en què s'ha fet el càlcul.

### Sintaxi

`x %= divisor; // equivalent a l'expressió x = x % divisor;`

### Paràmetres

`x`: variable. Tipus de dades permesos: int.  
`divisor`: variable o constant diferent de zero. Tipus de dades permesos: int.

### Exemple de codi

```
int x = 7;
x %= 5; // x ara conté 2
```

### Notes i advertències

L'operador mòdul compost no funciona amb floats.

Si el primer operand és negatiu, el resultat és negatiu (o zero). Per tant, el resultat de x %= 10 no sempre estarà entre 0 i 9 si x pot ser negatiu.

### Vegeu també

LLENGUATGE [Mòdul](../Operador-aritmetics/modul.md)  
LLENGUATGE [Estructura](../../Estructura.md)  
