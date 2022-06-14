---
títol: ">="
descripció: "major o igual que"
categoria: "Estructura"
subcategoria: "Operadors de comparació"
---

# >= (major o igual que)

## Descripció

Compara la variable de l'esquerra amb el valor o variable de la dreta de l'operador. Retorna cert quan l'operand de l'esquerra és més gran (més gran) o igual que l'operand de la dreta. Tingueu en compte que podeu comparar variables de diferents tipus de dades, però això podria generar resultats impredictibles; per tant, es recomana comparar variables del mateix tipus de dades, inclòs el tipus signed/unsigned.

### Sintaxi

`x >= y; // és cert si x és més gran o igual que y i és fals si x és menor que y`

### Paràmetres

`x`: variable. Tipus de dades permesos: int, float, double, byte, short, long.  
`y`: variable o constant. Tipus de dades permesos: int, float, double, byte, short, long.

### Exemple de codi

```
if (x >= y) { // prova si x és més gran (més gran) que o igual a y
   // fer alguna cosa només si el resultat de la comparació és cert
}
```

### Notes i advertències

Els nombres positius són més grans que els negatius.

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)  
