---
títol: "+"
descripció: "suma"
categoria: "Estructura"
subcategoria: "Operadors aritmètics"
---

# +

### Descripció

La suma és una de les quatre operacions aritmètiques primàries. L'operador + (plus) opera amb dos operands per produir la suma.

### Sintaxi

`sum = operand1 + operand2;`

### Paràmetres

`sum`: variable. Tipus de dades permesos: int, float, double, byte, short, long.  
`operand1`: variable o constant. Tipus de dades permesos: int, float, double, byte, short, long.  
`operand2`: variable o constant. Tipus de dades permesos: int, float, double, byte, short, long.

### Exemple de codi

```
int a = 5;
int b = 10;
int c = 0;
c = a + b; // la variable 'c' obté un valor de 15 després d'executar aquesta instrucció
```

### Notes i advertències

1. L'operació d'addició pot desbordar-se si el resultat és més gran que el que es pot emmagatzemar al tipus de dades (per exemple, afegir 1 a un nombre enter amb el valor 32.767 dóna -32.768).
2. Si un dels nombres (operands) és del tipus float o del tipus double, s'utilitzaran les matemàtiques de coma flotant per al càlcul.
3. Si els operands són de tipus de dades flotant / doble i la variable que emmagatzema la suma és un nombre enter, només s'emmagatzema la part integral i es perd la part fraccional del nombre.

```
float a = 5,5;
float b = 6,6;
int c = 0;
c = a + b; // la variable "c" només emmagatzema un valor de 12 en contraposició a la suma esperada de 12,1
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
