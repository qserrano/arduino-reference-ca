---
títol: "delay()"
descripció: ""
categoria: "Funcions"
subcategoria: "Temps"
---

# delay()

### Descripció

Pausa el programa per la quantitat de temps (en mil·lisegons) especificat com a paràmetre. (Hi ha 1000 mil·lisegons en un segon.)

### Sintaxi

`delay (ms)`

### Paràmetres

`ms`: el nombre de mil·lisegons per a fer una pausa. Tipus de dades permeses: unsigned long.

### Devolucions

Res

### Codi d'exemple

El codi deté el programa durant un segon abans d'alternar el pin d'eixida.

```
int ledPin = 13;              // LED connected to digital pin 13

void setup() {
  pinMode(ledPin, OUTPUT);    // sets the digital pin as output
}

void loop() {
  digitalWrite(ledPin, HIGH); // sets the LED on
  delay(1000);                // waits for a second
  digitalWrite(ledPin, LOW);  // sets the LED off
  delay(1000);                // waits for a second
}
```

### Notes i Advertiments

Si bé és fàcil crear un LED parpelletjant amb la funció de `delay()` i molts esbossos usen retards breus per a tasques com l'eliminació de rebots d'interruptors, l'ús de `delay()` en un sketch té importants inconvenients. Cap altra lectura de sensors, càlculs matemàtics o manipulació de pins pot continuar durant la funció de retard, per la qual cosa, en efecte, deté la majoria de les altres activitats. Per a obtindre enfocaments alternatius per a controlar el temps, consulte l’sketch **Blink Without Delay**, que realitza un cicle, sondejant la funció `millis()` fins que haja transcorregut suficient temps. Els programadors amb més
coneixements generalment eviten l'ús de `delay()` per a cronometrar esdeveniments de més de 10 mil·lisegons, llevat que l'sketch d'Arduino siga molt simple.

No obstant això, unes certes coses continuen mentre la funció de `delay()` controla el xip Atmega, perquè la funció de retard no desactiva les interrupcions. La comunicació en sèrie que apareix en el pin RX es registra, els valors PWM (analogWrite) i els estats del pin es mantenen, i les interrupcions funcionaran com deurien.

### Veure també

EXEMPLE [Blink Without Delay](http://arduino.cc/en/Tutorial/BlinkWithoutDelay) (en anglés)  
LLENGUATGE [Funcions](../../Funcions.md)
