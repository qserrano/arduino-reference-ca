---
títol: "loop()"
descripció: ""
categoria: "Estructura"
subcategoria: "Sketch"
---

# loop()

### Descripció

Després de crear una funció `setup()`, que inicialitza i estableix els valors inicials, la funció `loop()` fa precisament el que suggereix el seu nom i fa un bucle consecutivament, permetent que el vostre programa canviï i respongui. Utilitzeu-lo per controlar activament la placa Arduino.

### Exemple de codi

```
int buttonPin = 3;

// setup initializes serial and the button pin
void setup() {
  Serial.begin(9600);
  pinMode(buttonPin, INPUT);
}

// loop checks the button pin each time,
// and will send serial if it is pressed
void loop() {
  if (digitalRead(buttonPin) == HIGH) {
    Serial.write('H');
  }
  else {
    Serial.write('L');
  }

  delay(1000);
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
