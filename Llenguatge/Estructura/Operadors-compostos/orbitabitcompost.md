---
títol: "|="
descripció: "or compost per bits"
categoria: "Estructura"
subcategoria: "Operadors compostos"
---

# |=

### Descripció

L'operador OR compost per bits |= s'utilitza sovint amb una variable i una constant per "establir" (establir a 1) bits particulars en una variable.

Un repàs de l'OR | operador:

```
0 0 1 1 operand1
0 1 0 1 operand2
----------
0 1 1 1 (operand1 | operand2) - resultat retornat
```

### Sintaxi

`x |= y; // equivalent a x = x | y;`

### Paràmetres

`x`: variable. Tipus de dades permesos: char, int, long.  
`y`: variable o constant. Tipus de dades permesos: char, int, long.

### Exemple de codi

Els bits que tenen "OR de bits" amb 0 no es modifiquen, de manera que si myByte és una variable de bytes,

`myByte | 0b00000000 = myByte;`

Els bits que tenen "OR de bits" amb 1 s'estableixen a 1, de manera que:

`myByte | 0b11111111 = 0b11111111;`

### Notes i advertències

Com que estem tractant amb bits en un operador per bits, és convenient utilitzar el formatador binari amb constants. Els números segueixen sent el mateix valor en altres representacions, simplement no són tan fàcils d'entendre. A més, es mostra 0b00000000 per a més claredat, però zero en qualsevol format de nombre és zero.

En conseqüència, per establir els bits 0 i 1 d'una variable, sense canviar la resta de la variable, utilitzeu l'operador OR compost per bits (|=) amb la constant 0b00000011

```
1  0  1  0  1  0  1  0  variable
0  0  0  0  0  0  1  1  màscara
-----------------------
1  0  1  0  1  0  1  1

bits sense canvis
                  bits establerts
```

Aquí hi ha la mateixa representació amb els bits de variables substituïts pel símbol x

```
x  x  x  x  x  x  x  x  variable
0  0  0  0  0  0  1  1  màscara
-----------------------
x  x  x  x  x  x  1  1

bits sense canvis
                  bits establerts
```

Així que si:

```
myByte = 0b10101010;
myByte |= 0b00000011 == 0b10101011;
```

### Vegeu també

LLENGUATGE [| OR bit a bit](../Operadors-bitabit/bitabitor.md)  
LLENGUATGE [Estructura](../../Estructura.md)  
