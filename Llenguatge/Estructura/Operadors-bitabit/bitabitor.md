---
títol: "|"
descripció: "or bit a bit"
categoria: "Estructura"
subcategoria: "Operadors bit a bit"
---

# |

### Descripció

L'operador OR bit a bit en C++ és el símbol de la barra vertical, |. Igual que l'operador &, | opera de manera independent cada bit en les seves dues expressions enteres circumdants, però el que fa és diferent (per descomptat). L'OR bit a bit de dos bits és 1 si algun o tots dos bits d'entrada és 1, en cas contrari és 0.

En altres paraules:

```
0 0 1 1 operand1
0 1 0 1 operand2
----------
0 1 1 1 (operand1 | operand2) - resultat retornat
```

### Exemple de codi

```
int a = 92; // en binari: 0000000001011100
int b = 101; // en binari: 0000000001100101
int c = a | b; // resultat: 0000000001111101 o 125 en decimal.
```

Un dels usos més habituals de l'OR Bitwise és establir diversos bits en un nombre de bits.

```
// Nota: aquest codi és específic de l'arquitectura AVR
// estableix bits de direcció per als pins 2 a 7, deixa sense tocar PD0 i PD1 (xx | 00 == xx)
// igual que pinMode (pin, OUTPUT) per als pins 2 a 7 a Uno o Nano
DDRD = DDRD | 0b11111100;
```

### Vegeu també

EXEMPLE [Tutorial BitMath](https://www.arduino.cc/playground/Code/BitMath)  
LLENGUATGE [OR lògic](../Operadors-booleans/orlogic.md)  
LLENGUATGE [Estructura](../../Estructura.md)  
