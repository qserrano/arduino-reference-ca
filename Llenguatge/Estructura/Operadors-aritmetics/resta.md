---
títol: "-"
descripció: "resta"
categoria: "Estructura"
subcategoria: "Operadors aritmètics"
---

# -

### Descripció

La resta és una de les quatre operacions aritmètiques primàries. L'operador - (menys) opera amb dos operands per produir la diferència del segon amb el primer.

### Sintaxi

`difference = operand1 - operand2;`

### Paràmetres

`difference`: variable. Tipus de dades permesos: int, float, double, byte, short, long.  
`operand1`: variable o constant. Tipus de dades permesos: int, float, double, byte, short, long.  
`operand2`: variable o constant. Tipus de dades permesos: int, float, double, byte, short, long.

### Exemple de codi

```
int a = 5;
int b = 10;
int c = 0;
c = a - b;  // la variable 'c' obté un valor de -5 després d'executar aquesta instrucció
```

### Notes i advertències

1. L'operació de resta pot desbordar-se si el resultat és més petit que el que es pot emmagatzemar al tipus de dades (p. ex., restar 1 d'un nombre enter amb el valor -32.768 dóna 32.767).
2. Si un dels nombres (operands) és del tipus float o del tipus double, s'utilitzaran les matemàtiques de coma flotant per al càlcul.
3. Si els operands són de tipus de dades flotant/doble i la variable que emmagatzema la diferència és un enter, només s'emmagatzema la part integral i es perd la part fraccional del nombre.

```
float a = 5,5;
float b = 6,6;
int c = 0;
c = a - b; // la variable 'c' només emmagatzema un valor de -1 en oposició a la diferència esperada de -1,1
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
