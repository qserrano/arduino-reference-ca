---
títol: [const]
categoria: [ "Variables" ]
subcategoria: [ "Abast de variables" ]
---

# const

## Descripció

La paraula clau const significa constant. És un qualificador de variable que modifica el comportament de la variable, fent que una variable sigui "només de lectura". Això vol dir que la variable es pot utilitzar com qualsevol altra variable del seu tipus, però el seu valor no es pot canviar. Obtindreu un error del compilador si intenteu assignar un valor a una variable const.

Les constants definides amb la paraula clau const obeeixen les regles d'abast de variables que regeixen altres variables. Això, i els inconvenients d'utilitzar #define, fan que la paraula clau const sigui un mètode superior per definir constants i es prefereix a utilitzar #define.

## Exemple de codi

```
const float pi = 3,14;
float x;
// ....
x = pi * 2; // està bé utilitzar const en matemàtiques
pi = 7; // il·legal: no podeu escriure a (modificar) una constant
```
## Notes i advertències

**#define o const**  
Podeu utilitzar const o #define per crear constants numèriques o de cadena. Per a matrius, haureu d'utilitzar const. En general, es prefereix const sobre #define per definir constants.

## Vegeu també

LLENGUATGE [#define](../../Estructura/Sintaxi-adicional/define.md)  
LLENGUATGE [Variables](../../Variables.md)  
