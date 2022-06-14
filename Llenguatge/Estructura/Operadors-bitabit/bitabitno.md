---
títol: "~"
descripció: "not bit a bit"
categoria: "Estructura"
subcategoria: "Operadors bit a bit"
---

# ~

### Descripció

L'operador NOT bit a bit en C++ és el caràcter tilde ~. A diferència de & i |, l'operador NOT bit a bit s'aplica a un únic operand a la seva dreta. Bit a bit NO canvia cada bit al seu contrari: 0 es converteix en 1 i 1 es converteix en 0.

En altres paraules:

```
0 1 operand1
-----
1 0 ~operand1
```

### Exemple de codi

```
int a = 103; // binari: 0000000001100111
int b = ~a; // binari: 1111111110011000 = -104
```

### Notes i advertències

Potser us sorprendrà veure un nombre negatiu com -104 com a resultat d'aquesta operació. Això es deu al fet que el bit més alt d'una variable int és l'anomenat bit de signe. Si el bit més alt és 1, el nombre s'interpreta com a negatiu. Aquesta codificació de nombres positius i negatius es coneix com a complement de dos. Per a més informació, consulteu l'article de la Viquipèdia sobre el complement a dos.

A banda, és interessant observar que per a qualsevol nombre enter x, ~x és el mateix que -x - 1.

De vegades, el bit de signe en una expressió entera amb signe pot causar algunes sorpreses no desitjades.
Vegeu també

### Vegeu també

EXEMPLE [Tutorial BitMath](https://www.arduino.cc/playground/Code/BitMath)  
LLENGUATGE [Estructura](../../Estructura.md)  
