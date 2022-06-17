---
títol: "sq()"
descripció: ""
categoria: "Funcions"
subcategoria: "Matematiques"
---

# sq()

### Descripció

Calcula el quadrat d'un número: el número multiplicat per si mateix.

### Sintaxi

`sq(x)`

### Paràmetres

`x`: el número. Tipus de dades permeses: qualsevol tipus de dades.

### Devolucions

El quadrat del número. Tipus de dada: double.

### Notes i Advertiments

A causa de la forma en què s'implementa la funció `sq()`, evite usar altres funcions dins dels claudàtors, ja que pot generar resultats incorrectes.

Aquest codi llançarà resultats incorrectes:

```
int inputSquared = sq(Serial.parseInt()); // evitar aço
```

Usa això en el seu lloc:

```
int input = Serial.parseInt();  // mantindre les operacion fora de la funcio sq
int inputSquared = sq(input);
```

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
