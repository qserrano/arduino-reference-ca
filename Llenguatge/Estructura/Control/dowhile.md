---
títol: do...while
descripció: ""
categoria: "Estructura"
subcategoria: "Control"
---

# do...while

### Descripció

El cicle `do...while` funciona de la mateixa manera que el cicle `while`, amb l'excepció que la condició es prova al final del cicle, per la qual cosa el cicle `do` sempre s'executarà almenys una vegada.

### Sintaxi

```
do {
  // block d’instruccions
} while (condicio);
```

### Paràmetres

*  `condicio`: una expressió booleana que s'avalua com a vertadera o falsa.

### Codi d'exemple

```
int x = 0;
do {
  delay(50);          // esperar que els sensors s'estabilitzen
  x = readSensors();  // comprovar els sensors
} while (x < 100);
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
