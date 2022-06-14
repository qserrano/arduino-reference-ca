---
títol: ">>"
descripció: "mou a dreta bit a bit"
categoria: "Estructura"
subcategoria: "Operadors bit a bit"
---

# >>

### Descripció

L'operador de desplaçament a la dreta >> fa que els bits de l'operand esquerre es desplacin cap a la dreta en el nombre de posicions especificades per l'operand dret.

### Sintaxi

`variable >> nombre_de_bits;`  

### Paràmetres

`variable`: tipus de dades permesos: byte, int, long.  
`nombre_de_bits`: un nombre que és < = 32. Tipus de dades permesos: int.  

### Exemple de codi

```
  int a = 40; // binari: 0000000000101000
  int b = a >> 3; // binari: 0000000000000101 o 5 en decimal
```

### Notes i advertències

Quan desplaceu x a la dreta en y bits (x >> y) i el bit més alt de x és un 1, el comportament depèn del tipus de dades exacte de x. Si x és de tipus int, el bit més alt és el bit de signe, que determina si x és negatiu o no, com hem comentat anteriorment. En aquest cas, el bit de signe es copia en bits inferiors, per raons històriques esotèriques:

```
int x = -16; // binari: 1111111111110000
int y = 3;
int resultat = x >> y; // binari: 1111111111111110
```

Aquest comportament, anomenat extensió de signes, sovint no és el que voleu. En lloc d'això, potser voldreu que els zeros es desplacen des de l'esquerra. Resulta que les regles de desplaçament a la dreta són diferents per a les expressions int sense signe, de manera que podeu utilitzar un "typecast" per suprimir les que es copien des de l'esquerra:

```
int x = -16; // binari: 1111111111110000
int y = 3;
int resultat = (unsigned int)x >> y; // binari: 0001111111111110
```

Si teniu cura d'evitar l'extensió del signe, podeu utilitzar l'operador de desplaçament a la dreta >> com a forma de dividir per potències de 2. Per exemple:

```
int x = 1000;
int y = x >> 3; // divisió enter de 1000 per 8, fent que y = 125.
```

### Vegeu també

EXEMPLE [Tutorial BitMath](https://www.arduino.cc/playground/Code/BitMath)  
LLENGUATGE [Estructura](../../Estructura.md)  
