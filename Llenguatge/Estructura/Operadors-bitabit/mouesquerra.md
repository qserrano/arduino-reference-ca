---
títol: "<<"
descripció: "mou a esquerra bit a bit"
categoria: "Estructura"
subcategoria: "Operadors bit a bit"
---

# <<

### Descripció

L'operador de desplaçament a l'esquerra << fa que els bits de l'operand esquerre es desplacin cap a l'esquerra pel nombre de posicions especificades per l'operand dret.

### Sintaxi

`variable << nombre_de_bits;`

### Paràmetres

`variable`: tipus de dades permesos: byte, int, long.  
`nombre_de_bits`: un nombre que és < = 32. Tipus de dades permesos: int.

### Exemple de codi

```
int a = 5; // binari: 0000000000000101
int b = a << 3; // binari: 0000000000101000 o 40 en decimal
```

### Notes i advertències

Quan canvieu un valor x per y bits (x << y), els y bits més a l'esquerra de x es perden, literalment desplaçats fora de l'existència:

```
int x = 5; // binari: 0000000000000101
int y = 14;
int resultat = x << y; // binari: 0100000000000000 - el primer 1 de 101 es va descartar
```

Si esteu segurs que cap dels d'un valor s'està desplaçant a l'oblit, una manera senzilla de pensar en l'operador de desplaçament a l'esquerra és que multiplica l'operand esquerre per 2 elevat a la potència de l'operand dret. Per exemple, per generar potències de 2, es poden utilitzar les expressions següents:

```
   Resultat de l'operació
   --------- ------
    1 << 0 1
    1 << 1 2
    1 << 2 4
    1 << 3 8
    ...
    1 << 8 256
    1 << 9 512
    1 << 10 1024
    ...
```

L'exemple següent es pot utilitzar per imprimir el valor d'un byte rebut al monitor sèrie, utilitzant l'operador de desplaçament esquerre per moure's al llarg del byte de baix (LSB) a dalt (MSB) i imprimir el seu valor binari:

```
// Imprimeix el valor binari (1 o 0) del byte
void printOut1(int c) {
  for (int bits = 7; bits > -1; bits--) {
    // Compara els bits 7-0 en byte
    if (c & (1 << bits)) {
      Serial.print("1");
    }
    altrament {
      Serial.print("0");
    }
  }
}
```

### Vegeu també

EXEMPLE [Tutorial BitMath](https://www.arduino.cc/playground/Code/BitMath)  
LLENGUATGE [Estructura](../../Estructura.md)  
