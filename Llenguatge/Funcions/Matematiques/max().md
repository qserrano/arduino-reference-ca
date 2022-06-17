---
títol: "max()"
descripció: ""
categoria: "Funcions"
subcategoria: "Matematiques"
---

# max()

### Descripció

Calcula el màxim de dos números.

### Sintaxi

`max(x, y)`

### Paràmetres

`x`: el primer número. Tipus de dades permeses: qualsevol tipus de dades.  
`y`: el segon número. Tipus de dades permeses: qualsevol tipus de dades.  

### Devolucions

El major dels dos valors de paràmetre.

### Codi d'exemple

El codi assegura que sensVal siga almenys 20.

```
sensVal = max(sensVal, 20); // assigna sensVal al més gran entre sensVal o 20
                            // (assegurant-se de manera efectiva que sigui almenys 20)
```

### Notes i Advertiments

Tal vegada en contra de la intuïció, `max()` s'usa sovint per a restringir l'extrem inferior del rang d'una variable, mentre que `min()` s'usa per a restringir l'extrem superior del rang.

A causa de la forma en què s'implementa la funció `max()`, evite usar altres funcions dins dels claudàtors, ja que pot generar resultats incorrectes.

```
max(a--, 0);  // evitar-ho: dóna resultats incorrectes

// usa açò al seu lloc
max(a, 0);
a--;  // mantingueu altres funcions fora de max()
```

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)  
