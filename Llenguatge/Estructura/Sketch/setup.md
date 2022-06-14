---
títol: "setup()"
descripció: ""
categoria: "Estructura"
subcategoria: "Sketch"
---

# setup()

### Descripció

La funció `setup()` es crida quan comença un esbós. Utilitzeu-lo per inicialitzar variables, modes de pin, començar a utilitzar biblioteques, etc. La funció `setup()` només s'executarà una vegada, després de cada engegada o restabliment de la placa Arduino.

### Exemple de codi

```
int buttonPin = 3;

void setup() {
  Serial.begin(9600);
  pinMode(buttonPin, INPUT);
}

void loop() {
  // ...
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
