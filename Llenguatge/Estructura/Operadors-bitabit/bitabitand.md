---
títol: "&"
descripció: "and bit a bit"
categoria: "Estructura"
subcategoria: "Operadors bit a bit"
---

# &

### Descripció

L'operador AND bit a bit en C++ és un & ampersand únic, utilitzat entre altres dues expressions senceres. L'AND bit a bit opera en cada posició de bit de les expressions circumdants de manera independent, d'acord amb aquesta regla: si els dos bits d'entrada són 1, la sortida resultant és 1, en cas contrari la sortida és 0.

Una altra manera d'expressar-ho és:

```
0 0 1 1 operand1  
0 1 0 1 operand2  
\----------  
0 0 0 1 (operand1 i operand2) - resultat retornat
```

A Arduino, el tipus int és un valor de 16 bits, de manera que l'ús de & entre dues expressions int fa que es produeixin 16 operacions AND simultànies.

### Exemple de codi

En un fragment de codi com:

```
int a = 92; // en binari: 0000000001011100
int b = 101; // en binari: 0000000001100101
int c = a & b; // resultat: 0000000001000100 o 68 en decimal.
```

Cadascun dels 16 bits d'a i b es processen utilitzant l'AND bit a bit, i els 16 bits resultants s'emmagatzemen a c, donant com a resultat el valor 01000100 en binari, que és 68 en decimal.

Un dels usos més habituals de AND bit a bit és seleccionar un bit (o bits) en particular d'un valor enter, sovint anomenat emmascarament. Vegeu a continuació un exemple (específic de l'arquitectura AVR).

`PORTD = PORTD & 0b00000011; // esborra els bits 2 - 7, deixa els pins PD0 i PD1 sense tocar (xx i 11 == xx)`

### Vegeu també

EXEMPLE [Tutorial BitMath](https://www.arduino.cc/playground/Code/BitMath)  
LLENGUATGE [&& AND lògic](../Operadors-booleans/andlogic.md)  
LLENGUATGE [Estructura](../../Estructura.md)  
