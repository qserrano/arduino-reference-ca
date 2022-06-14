---
títol: break
descripció: ""
categoria: "Estructura"
subcategoria: "Control"
---


# break

### Descripció

`break` s'utilitza per eixir d'un bucle `for`, `while` o `do...while`, obviant la condició normal del bucle. També s'utilitza per eixir d'una instrucció `switch case`.

### Exemple de codi

```
int threshold = 40;
for (int x = 0; x < 255; x++) {
  analogWrite(PWMpin, x);
  sens = analogRead(sensorPin);
  if (sens > threshold) {     // si es supera el límit
    x = 0;
    break;
  }
  delay(50);
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
