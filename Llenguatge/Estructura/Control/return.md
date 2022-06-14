---
títol: return
descripció: ""
categoria: "Estructura"
subcategoria: "Control"
---

# return

### Descripció

Finalitze una funció i retorne un valor d'una funció a la funció que anomena, si ho desitja.

### Sintaxi

`return;`  
`return value;`

### Paràmetres

`value`: Tipus de dades permeses: qualsevol variable o tipus constant.

### Codi d'exemple

Una funció per a comparar l'entrada d'un sensor amb un llindar

```
int checkSensor() {
  if (analogRead(0) > 400) {
    return 1;
  }
  else {
    return 0;
  }
}
```

La paraula clau de retorn és útil per a provar una secció de codi sense haver de "comentar" grans seccions de codi possiblement amb errors.

```
void loop() {
  // provar aqui la idea brillant de codi

  return;

  // la resta d’un esbos disfuncional aqui
  // aquest codi no s’executara mai
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
