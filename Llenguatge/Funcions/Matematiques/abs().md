---
títol: "abs()"
descripció: ""
categoria: "Funcions"
subcategoria: "Matematiques"
---

# abs()

### Descripció

Calcula el valor absolut d'un número.

### Sintaxi

`abs(x)`

### Paràmetres

`x`: el número

### Devolucions

x: si `x` és major o igual a 0.  
-x: si `x` és menor que 0.

### Codi d'exemple

Imprimeix el valor absolut de la variable x en el monitor serie.

```
void setup() {
  Serial.begin(9600);
  while (!Serial) {
    ;  // espera per a la connexió del port serie. Necessari només per al port natiu USB
  }
  int x = 42;
  Serial.print("El valor absolut de ");
  Serial.print(x);
  Serial.print(" és ");
  Serial.println(abs(x));
  x = -42;
  Serial.print("El valor absolut de ");
  Serial.print(x);
  Serial.print(" és ");
  Serial.println(abs(x));
}

void loop() {
}
```

### Notes i Advertiments

A causa de la forma en què s'implementa la funció abs(), evite usar altres funcions dins dels claudàtors,
ja que pot generar resultats incorrectes.

```
abs(a++); // evitar-ho: dóna resultats incorrectes

// utilitzar això en el seu lloc:
abs(a);
a++;  // mantenir altres funcions matemàtiques fora de la funció
```
### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
