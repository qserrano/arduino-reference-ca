---
títol: "micros()"
descripció: ""
categoria: "Funcions"
subcategoria: "Temps"
---

# micros()

### Descripció

Retorna el nombre de microsegons des que la placa Arduino va començar a executar el programa actual. Aquest número es desbordarà (tornarà a zero) després d'aproximadament 70 minuts. En les plaques de la família Arduino Portenta aquesta funció té una resolució d'un microsegon en tots els nuclis. En plaques Arduino de 16 MHz (per exemple, Duemilanove i Nano), aquesta funció té una resolució de quatre microsegons (és a dir, el valor retornat és sempre un múltiple de quatre). En plaques Arduino de 8 MHz (per exemple, LilyPad), aquesta funció té una resolució de huit microsegons.

### Sintaxi

`time = micros()`

### Paràmetres

Cap

### Devolucions

Retorna el nombre de microsegons des que la placa Arduino va començar a executar el programa actual. Tipus de dades: unsigned long

### Codi d'exemple

El codi retorna el nombre de microsegons des que va començar la placa Arduino.

```
unsigned long time;

void setup() {
  Serial.begin(9600);
}
void loop() {
  Serial.print("Time: ");
  time = micros();

  Serial.println(time); //prints time since program started
  delay(1000);          // wait a second so as not to send massive amounts of data
}
```

### Notes i advertències

Hi ha 1.000 microsegons en un mil·lisegon i 1.000.000 de microsegons en un segon.

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
