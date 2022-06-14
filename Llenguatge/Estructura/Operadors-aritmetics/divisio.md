---
títol: "/"
descripció: "divisió"
categoria: "Estructura"
subcategoria: "Operadors aritmètics"
---

# /

### Descripció

La divisió és una de les quatre operacions aritmètiques primàries. L'operador / (barra inclinada) opera sobre dos operands per produir el resultat.

### Sintaxi

`result = numerator / denominator;`

### Paràmetres

`result`: variable. Tipus de dades permesos: int, float, double, byte, short, long.  
`numerator`: variable o constant. Tipus de dades permesos: int, float, double, byte, short, long.  
`denominator`: variable o constant diferent de zero. Tipus de dades permesos: int, float, double, byte, short, long.

### Exemple de codi

```
int a = 50;
int b = 10;
int c = 0;
c = a / b; // la variable 'c' obté un valor de 5 després d'executar aquesta instrucció
```

### Notes i advertències

1. Si un dels nombres (operands) és del tipus float o del tipus double, s'utilitzaran les matemàtiques de coma flotant per al càlcul.
2. Si els operands són de tipus de dades flotant/doble i la variable que emmagatzema el resultat és un nombre enter, només s'emmagatzema la part integral i es perd la part fraccional del nombre.

```
float a = 55,5;
float b = 6,6;
int c = 0;
c = a / b; // la variable 'c' només emmagatzema un valor de 8 a diferència del resultat esperat de 8.409
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
