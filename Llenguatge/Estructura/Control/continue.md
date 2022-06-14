---
títol: continue
descripció: ""
categoria: "Estructura"
subcategoria: "Control"
---

# continue

### Descripció

La instrucció `continue` salta la resta de la iteració actual d'un bucle (`for`, `while`, o `do ... while`). Continua verificant l'expressió condicional del bucle i procedint amb qualsevol iteració posterior.

### Codi d'exemple

El següent codi escriu el valor de 0 a 255 a la PWMPIN, però salta els valors en el rang de 41 a 119.

```
for (int x = 0; x <= 255; x ++) {
  if (x > 40 && x < 120) {  // crea el salt entre els valors
    continue;
  }

  analogWrite(PWMpin, x);
  delay(50);
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
