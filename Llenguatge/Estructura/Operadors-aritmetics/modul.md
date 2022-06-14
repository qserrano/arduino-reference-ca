---
títol: "%"
descripció: "mòdul"
categoria: "Estructura"
subcategoria: "Operadors aritmètics"
---

# %

### Descripció

L’operador de mòdul calcula la resta quan un nombre enter es divideix per un altre. És útil per mantenir una variable dins d'un rang determinat (per exemple, la mida d'una matriu). El símbol % (per cent) s'utilitza per dur a terme l'operació de mòdul.

### Sintaxi

`remainder = dividend % divisor;`

### Paràmetres

`remainder`: variable. Tipus de dades permesos: int, float, double.  
`dividend`: variable o constant. Tipus de dades permesos: int.  
`divisor`: variable o constant diferent de zero. Tipus de dades permesos: int.  

### Exemple de codi

```
int x = 0;
x = 7 % 5;  // x ara conté 2
x = 9 % 5;  // x ara conté 4
x = 5 % 5;  // x ara conté 0
x = 4 % 5;  // x ara conté 4
x = -4 % 5; // x ara conté-4
x = 4 % -5; // x ara conté 4
```

```
/* actualitza un valor en una matriu cada vegada mitjançant un bucle */

int values[10];
int i = 0;

void setup() {}

void loop() {
  values[i] = analogRead(0);
  i = (i + 1) % 10; // L'operador de la resta passa sobre la variable
}
```

### Notes i advertències

1. L'operador módul no treballa amb floats.
2. Si el primer operand és negatiu, el resultat és negatiu (o zero). Per tant, el resultat de x % 10 no sempre estarà entre 0 i 9 si x pot ser negatiu.

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
