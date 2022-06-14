---
títol: "&="
descripció: "and compost"
categoria: "Estructura"
subcategoria: "Operadors compostos"
---

# &=

### Descripció

L'operador AND compost per bits &= s'utilitza sovint amb una variable i una constant per forçar bits particulars d'una variable a l'estat BAIX (a 0). Sovint, a les guies de programació, això s'anomena "esborrar" o "restablir" bits.

Una revisió de l'operador & Bitwise AND:

```
0 0 1 1 operand1
0 1 0 1 operand2
----------
0 0 0 1 (operand1 i operand2): resultat retornat
```

### Sintaxi

`x &= y; // equivalent a x = x & y;`

### Paràmetres

`x`: variable. Tipus de dades permesos: char, int, long.  
`y`: variable o constant. Tipus de dades permesos: char, int, long.

### Exemple de codi

Els bits que tenen un "AND" per bits amb 0 s'esborren a 0, per tant, si myByte és una variable de bytes,

```
myByte & 0b00000000 = 0;
```

Els bits que tenen "AND de bits" amb 1 no es modifiquen, per tant,

```
myByte & 0b11111111 = myByte;
```

### Notes i advertències

Com que estem tractant amb bits en un operador per bits, és convenient utilitzar el formatador binari amb constants. Els números segueixen sent el mateix valor en altres representacions, simplement no són tan fàcils d'entendre. A més, es mostra 0b00000000 per a més claredat, però zero en qualsevol format de nombre és zero (hmmm hi ha alguna cosa filosòfica?)

En conseqüència, per esborrar (establir a zero) els bits 0 i 1 d'una variable, sense canviar la resta de la variable, utilitzeu l'operador AND compost per bits (&=) amb la constant 0b11111100

```
1  0  1  0  1  0  1  0  variable
1  1  1  1  1  1  0  0  màscara
-----------------------
1  0  1  0  1  0  0  0
```

```
bits sense canvis
                  bits esborrats
```

Aquí hi ha la mateixa representació amb els bits de la variable substituïts pel símbol x

```
x  x  x  x  x  x  x  x  variable
1  1  1  1  1  1  0  0  màscara
-----------------------
x  x  x  x  x  x  0  0
```
```
bits sense canvis
                  bits esborrats
```

Així que si:

```
myByte = 0b10101010;
myByte &= 0b11111100; // resulta en 0b10101000
```

### Vegeu també

LLENGUATE [& Bit a bit](../Operadors-bitabit/bitabitand.md)  
LLENGUATGE [Estructura](../../Estructura.md)  
