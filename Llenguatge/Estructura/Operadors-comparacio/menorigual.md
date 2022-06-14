---
títol: "<="
descripció: "menor o igual que"
categoria: "Estructura"
subcategoria: "Operadors de comparació"
---

# <=

### Descripció

Compara la variable de l'esquerra amb el valor o variable de la dreta de l'operador. Retorna cert quan l'operand de l'esquerra és menor (més petit) o igual que l'operand de la dreta. Tingueu en compte que podeu comparar variables de diferents tipus de dades, però això podria generar resultats impredictibles; per tant, es recomana comparar variables del mateix tipus de dades, inclòs el tipus signat/sense signar.

### Sintaxi

`x ⇐ y; // és cert si x és menor o igual que y i és fals si x és major que y`

### Paràmetres

`x`: variable. Tipus de dades permesos: int, float, double, byte, short, long.  
`y`: variable o constant. Tipus de dades permesos: int, float, double, byte, short, long.

### Exemple de codi

```
if (x <= y) { // prova si x és menor (menor) que o igual a y
   // fer alguna cosa només si el resultat de la comparació és cert
}
```

### Notes i advertències

Els nombres negatius són més petits que els nombres positius.

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)  
