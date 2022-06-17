---
títol: "min()"
descripció: ""
categoria: "Funcions"
subcategoria: "Matematiques"
---

# min()

### Descripció

Calcula el mínim de dos números.

### Sintaxi

`min(x, y)`

### Paràmetres

`x`: el primer número. Tipus de dades permeses: qualsevol tipus de dades.  
`y`: el segon número. Tipus de dades permeses: qualsevol tipus de dades.

### Devolucions

El menor dels dos números.

### Codi d'exemple

El codi assegura que mai supere 100.

```
sensVal = min(sensVal, 100);  // assigna a sensVal el menor valor entre sensVal o 100
                              // assegurant-se que mai sera major que 100
```

### Notes i Advertiments

Tal vegada en contra de la intuïció, max() s'usa sovint per a restringir l'extrem inferior del rang d'una variable, mentre que min() s'usa per a restringir l'extrem superior del rang.

A causa de la forma en què s'implementa la funció min(), evite usar altres funcions dins dels claudàtors, ja que pot generar resultats incorrectes.

```
min(a++, 100);  // evitar-ho: dóna resultats incorrectes

min(a, 100);    // utilitzeu-ho en el seu lloc: mantingueu altres operacions matemàtiques
a++;            // fora de la funció
```

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
