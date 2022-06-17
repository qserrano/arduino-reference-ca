---
títol: "digitalRead()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Digitals"
---

# digitalRead()

### Descripció

Llig el valor d'un pin digital especificat, ja siga HIGH o LOW.

### Sintaxi

`digitalRead (pin)`

### Paràmetres

`pin`: el número de pin d'Arduino que desitja llegir

### Devolucions

HIGH o LOW

### Codi d'exemple

Estableix el pin 13 al mateix valor que el pin 7, declarat com a entrada.

```
int ledPin = 13;  // LED connectat al pin digital 13
int inPin = 7;    // polsador connectat al pin digital 7
int val = 0;      // variable per a emmagatzemar el valor llegit
void setup() {
  pinMode(ledPin, OUTPUT);  // estableix el pin digital 13 com a eixida
  pinMode(inPin, INPUT);    // estableix el pin digital 7 com a entrada
}
void loop() {
  val = digitalRead(inPin);   // llig el pin d'entrada
  digitalWrite(ledPin, val);  // estableix el LED al valor del botó
}
```

### Notes i Advertiments

Si el pin no està connectat a res, digitalRead() pot retornar HIGH o LOW (i això pot canviar aleatòriament).

Els pins d'entrada analògica es poden usar com a pins digitals, denominats A0, A1, etc. L'excepció són els pins A6 i A7 d'Arduino Nano, Pro Mini i Mini, que només es poden usar com a entrades analògiques.

### Veure també

EXEMPLE link: [Descripció dels pins digitals (en anglés)](http://arduino.cc/en/Tutorial/DigitalPins)  
LLENGUATGE [Funcions](../../Funcions.md)
