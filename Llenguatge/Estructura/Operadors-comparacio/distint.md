---
títol: "!="
descripció: "distint"
categoria: "Estructura"
subcategoria: "Operadors de comparació"
---

# !=

### Descripció

Compara la variable de l'esquerra amb el valor o variable de la dreta de l'operador. Retorna cert quan els dos operands no són iguals. Tingueu en compte que podeu comparar variables de diferents tipus de dades, però això podria generar resultats impredictibles; per tant, es recomana comparar variables del mateix tipus de dades, inclòs el tipus signed/unsigned.

### Sintaxi

`x != y; // és fals si x és igual a y i és cert si x no és igual a y`

### Paràmetres

`x`: variable. Tipus de dades permesos: int, float, double, byte, short, long.  
`y`: variable o constant. Tipus de dades permesos: int, float, double, byte, short, long.

### Exemple de codi

```
if (x != y) { // prova si x no és igual a y
   // fer alguna cosa només si el resultat de la comparació és cert
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)  
