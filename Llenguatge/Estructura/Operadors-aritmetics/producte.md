---
títol: "*"
descripció: "producte"
categoria: "Estructura"
subcategoria: "Operadors aritmètics"
---

# *

### Descripció

La multiplicació és una de les quatre operacions aritmètiques primàries. L'operador * (asterisc) opera amb dos operands per obtindre el producte.

### Sintaxi

`product = operand1 * operand2;`

### Paràmetres

`product`: variable. Tipus de dades permesos: int, float, double, byte, short, long.  
`operand1`: variable o constant. Tipus de dades permesos: int, float, double, byte, short, long.  
`operand2`: variable o constant. Tipus de dades permesos: int, float, double, byte, short, long.  

### Exemple de codi

```
int a = 5;
int b = 10;
int c = 0;
c = a * b; // la variable 'c' obté un valor de 50 després d'executar aquesta instrucció
```

### Notes i advertències

1. L'operació de multiplicació pot desbordar-se si el resultat és més gran que el que es pot emmagatzemar al tipus de dades.
2. Si un dels nombres (operands) és del tipus float o del tipus double, s'utilitzaran les matemàtiques de coma flotant per al càlcul.
3. Si els operands són de tipus de dades flotant / doble i la variable que emmagatzema el producte és un nombre enter, només s'emmagatzema la part integral i es perd la part fraccional del nombre.

```
float a = 5,5;
float b = 6,6;
int c = 0;
c = a * b; // la variable 'c' només emmagatzema un valor de 36 en contraposició al producte esperat de 36,3
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
