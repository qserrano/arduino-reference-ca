---
títol: "bool"
categories: [ "Variables" ]
subcategories: [ "Tipus de dades" ]
---

# bool

### Descripció

Una variable `bool` conté un de dos valors, vertader o fals. (Cada variable `bool` ocupa un byte de memòria).

### Sintaxi

`bool var = valor;`

### Paràmetres

`var`: nom de la variable.  
`val`: el valor a assignar a aqueixa variable.

### Codi d'exemple

Aquest codi mostra com usar el tipus de dades bool.

```
int LEDpin = 5;     // LED on pin 5
int switchPin = 13; // momentary switch on 13, other side connected to ground

bool running = false;

void setup() {
  pinMode(LEDpin, OUTPUT);
  pinMode(switchPin, INPUT);
  digitalWrite(switchPin, HIGH);  // turn on pullup resistor
}

void loop() {
  if (digitalRead(switchPin) == LOW) {
    // switch is pressed - pullup keeps pin high normally
    delay(100);                     // delay to debounce switch
    running = !running;             // toggle running variable
    digitalWrite(LEDpin, running);  // indicate via LED
  }
}
```

### Veure també

LLENGUATGE [constants](../Constants/constants.md)   
LLENGUATGE [Variables](../../Variables.md)
