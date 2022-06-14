---
títol: switch...case
descripció: ""
categoria: "Estructura"
subcategoria: "Control"
---

# switch...case

### Descripció

Igual que les declaracions `if`, `switch case` controla el flux de programes en permetre que els programadors especifiquen diferents codis que han d'executar-se en diverses condicions. En particular, una sentència switch compara el valor d'una variable amb els valors especificats en sentències case. Quan es troba una declaració de case el valor del qual coincideix amb el de la variable, s'executa el codi en aqueixa declaració de case.

La paraula clau break ix de la instrucció switch i normalment s'usa al final de cada cas. Sense una sentència break, la sentència switch continuarà executant les següents expressions ("falling-through") fins que s'aconseguisca un trencament o el final de la sentència switch.

### Sintaxi

```
switch (var) {
  case label1:
    // declaracions
    break;
  case label2:
    // declaracions
    break;
  default:
    // declaracions
    break;
}
```

### Paràmetres

`var`: una variable el valor de la qual comparar amb diversos casos. Tipus de dades permeses: int, char.  
`label1`, `label2`: constants. Tipus de dades permeses: int, char.

### Devolucions

Res

### Codi d'exemple

```
switch (var) {
  case 1:
    //er alguna cosa quan var és igual a 1
    break;
  case 2:
    //er alguna cosa quan var és igual a 2
    break;
  default:
    // si res més coincideix, fes el predeterminat
    // default es opcional
    break;
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
