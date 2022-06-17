---
títol: "constrain()"
descripció: ""
categoria: "Funcions"
subcategoria: "Matematiques"
---

# constrain()

### Descripció

Restringeix un número perquè estiga dins d'un rang.

### Sintaxi

`constrain (x, a, b)`

### Paràmetres

`x`: el número a restringir. Tipus de dades permeses: tots els tipus de dades.  
`a`: l'extrem inferior del rang. Tipus de dades permeses: tots els tipus de dades.  
`b`: l'extrem superior del rang. Tipus de dades permeses: tots els tipus de dades.

### Devolucions

x: si x està entre a i b.  
a: si x és menor que a.  
b: si x és major que b.

### Codi d'exemple

El codi limita els valors del sensor entre 10 i 150.

`sensVal = constrain(sensVal, 10, 150);  `

### Notes i Advertiments

A causa de la forma en què s'implementa la funció `constrain()`, evite usar altres funcions dins dels claudàtors, ja que pot generar resultats incorrectes.

Aquest codi llançarà resultats incorrectes:

```
int constrainedInput = constrain(Serial.parseInt(), minimumValue, maximumValue);  // evitar això
```

Usa això en el seu lloc:

```
int input = Serial.parseInt();  // mantingue les altres operacions fora de la funcio constrain
int constrainedInput = constrain(input, minimumValue, maximumValue);
```
### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
