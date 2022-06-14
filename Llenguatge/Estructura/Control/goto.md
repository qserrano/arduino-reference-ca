---
títol: goto
descripció: ""
categoria: "Estructura"
subcategoria: "Control"
---

# goto

### Descripció

Transfereix el flux del programa a un punt etiquetat en el programa

### Sintaxi

`label:`  
`goto label;` // envia el fluxe de programa a label

### Codi d'exemple

```
  for (byte g = 255; g > 0; g--) {
    for (byte b = 0; b < 255; b++) {
      if (analogRead(0) > 250) {
        goto bailout;
      }
      // més instruccions ...
    }
  }
}

bailout:
// mes instruccions ...
```

### Notes i Advertiments

Es desaconsella l'ús de goto en la programació en C, i alguns autors de llibres de programació en C afirmen que la instrucció goto mai és necessària, però si s'usa amb prudència, pot simplificar uns certs programes. La raó per la qual molts programadors desaproven l'ús de goto és que amb l'ús desenfrenat de sentències goto, és fàcil crear un programa amb un flux de programa indefinit, que mai es pot depurar.

Dit això, hi ha casos en els quals una instrucció goto pot ser útil i simplificar la codificació. Una d'aquestes situacions és eixir de bucles for profundament niats, o si la lògica es bloqueja, en una determinada condició.

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
