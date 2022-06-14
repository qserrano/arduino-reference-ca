---
títol: "*"
descripció: "indireccio"
categoria: "Estructura"
subcategoria: "Operadors amb punters"
---

# *

### Descripció

La indirecció (desreferenciació) és una de les característiques específicament per utilitzar amb punters. Per a aquest propòsit s'utilitza l'operador asterisc *. Si p és un punter, aleshores *p representa el valor contingut a l'adreça assenyalada per p.

### Exemple de codi

```
int *p; // declara un punter a un tipus de dades int
int i = 5;
int resultat = 0;
p = &i; // ara 'p' conté l'adreça de 'i'
resultat = *p; // 'resultat' obté el valor a l'adreça apuntada per 'p'
               // és a dir, obté el valor de 'i' que és 5
```

### Notes i advertències

Els punters són un dels temes complicats per als principiants en l'aprenentatge de C, i és possible escriure la gran majoria dels esbossos d'Arduino sense trobar-hi mai punters. Tanmateix, per manipular determinades estructures de dades, l'ús de punters pot simplificar el codi, i el coneixement de la manipulació de punters és útil tenir al conjunt d'eines.

### Vegeu també

DEFINICIO [Punters](https://en.wikipedia.org/wiki/Pointer_%28computer_programming%29)  
LLENGUATGE [Estructura](../../Estructura.md)  
