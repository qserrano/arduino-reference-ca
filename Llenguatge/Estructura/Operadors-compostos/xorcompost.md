---
títol: "^="
descripció: "xor compost"
categoria: "Estructura"
subcategoria: "Operadors compostos"
---

# ^=

### Descripció

L'operador XOR compost per bits ^= s'utilitza sovint amb una variable i una constant per canviar (invertir) bits particulars en una variable.

Una repàs de l'operador Bitwise XOR ^:

```
0 0 1 1 operand1
0 1 0 1 operand2
----------
0 1 1 0 (operand1 ^ operand2) - resultat retornat
```

### Sintaxi

`x ^= y; // equivalent a x = x ^ y;`

### Paràmetres

`x`: variable. Tipus de dades permesos: char, int, long.  
`y`: variable o constant. Tipus de dades permesos: char, int, long.

### Exemple de codi

Els bits operats per XOR bit a bit amb 0 en la màscara es deixen sense canvis. Així, si myByte és una variable de bytes,

`myByte ^ 0b00000000 = myByte;`

Els bits operats per XOR bit a bit amb 1 en la màscara es canvien així:

`myByte ^ 0b11111111 = ~myByte;`

### Notes i advertències

Com que estem tractant amb bits en un operador per bits, és convenient utilitzar el formatador binari amb constants. Els números segueixen sent el mateix valor en altres representacions, simplement no són tan fàcils d'entendre. A més, es mostra 0b00000000 per a més claredat, però zero en qualsevol format de nombre és zero.

En conseqüència, per alternar els bits 0 i 1 d'una variable, sense canviar la resta de la variable, utilitzeu l'operador XOR compost per bits (^=) amb la constant 0b00000011

```
1  0  1  0  1  0  1  0  variable
0  0  0  0  0  0  1  1  màscara
-----------------------
1  0  1  0  1  0  0  1

bits sense canvis
                  bits alternats
```

Aquí hi ha la mateixa representació amb els bits de variables substituïts pel símbol x. ~x representa el complement de x.

```
x  x  x  x  x  x  x  x  variable
0  0  0  0  0  0  1  1  màscara
-----------------------
x  x  x  x  x  x ~x ~x

bits sense canvis
                  bits establerts
```

Així que si:

```
myByte = 0b10101010;
myByte ^= 0b00000011 == 0b10101001;
```

### Vegeu també

LLENGUATGE [^ XOR bit a bit](../Operadors-bitabit/xor.md)  
LLENGUATGE [Estructura](../../Estructura.md)  
