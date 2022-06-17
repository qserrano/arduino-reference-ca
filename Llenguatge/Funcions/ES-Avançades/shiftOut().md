---
títol: "shiftOut()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Avançades"
---

# shiftOut()

### Descripció

Desplaça un byte de dades un bit cada vegada. Comença des del bit més significatiu (és a dir, el més a l'esquerra) o menys (el més a la dreta). Cada bit s'escriu al seu torn en un pin de dades, després de la qual cosa es prem un pin de rellotge (es pren alt, després baix) per a indicar que el bit està disponible.

**Nota**: si està interactuant amb un dispositiu que té un rellotge amb flancs ascendents, haurà d'assegurar-se que el pin del rellotge estiga baix abans de cridar a `shiftOut()`, p.e. amb una crida a `digitalWrite(clockPin, LOW)`.

Aquesta és una implementació de programari; consulte també la [biblioteca SPI](https://www.arduino.cc/en/Reference/SPI), que proporciona una implementació de maquinari que és més ràpida però funciona només en pins específics.

### Sintaxi

`shiftOut(dataPin, clockPin, bitOrder, value)`

### Paràmetres

`dataPin`: el pin en el qual generar cada bit. Tipus de dades permeses: int.  
`clockPin`: el pin per a alternar una vegada que el pin de dades s'haja establit en el valor correcte. Tipus de dades permeses: int.  
`bitOrder`: en quin ordre desplaçar els bits; ja siga MSBFIRST o LSBFIRST. (Primer el bit més significatiu o Primer el bit menys significatiu).  
`value`: les dades a desplaçar. Tipus de dades permeses: byte.  

### Devolucions

Res

### Codi d'exemple

Per a conéixer el circuit adjunt, consulte el [tutorial sobre el control d'un registre de desplaçament 74HC595](https://arduino.cc/en/Tutorial/ShiftOut).
(en anglés)

```
//**************************************************************//
//  Name    : shiftOutCode, Hello World                         //
//  Author  : Carlyn Maw,Tom Igoe                               //
//  Date    : 25 Oct, 2006                                      //
//  Version : 1.0                                               //
//  Notes   : Code for using a 74HC595 Shift Register           //
//          : to count from 0 to 255                            //
//****************************************************************

//Pin connected to ST_CP of 74HC595
int latchPin = 8;
//Pin connected to SH_CP of 74HC595
int clockPin = 12;
////Pin connected to DS of 74HC595
int dataPin = 11;

void setup() {
  //set pins to output because they are addressed in the main loop
  pinMode(latchPin, OUTPUT);
  pinMode(clockPin, OUTPUT);
  pinMode(dataPin, OUTPUT);
}

void loop() {
  //count up routine
  for (int j = 0; j < 256; j++) {
    //ground latchPin and hold low for as long as you are transmitting
    digitalWrite(latchPin, LOW);
    shiftOut(dataPin, clockPin, LSBFIRST, j);
    //return the latch pin high to signal chip that it
    //no longer needs to listen for information
    digitalWrite(latchPin, HIGH);
    delay(1000);
  }
}
```

### Notes i Advertiments

El pin de dades i el pin de rellotge ja han d'estar configurats com a eixides mitjançant una anomenada a `pinMode()`.

`shiftOut()` actualment està escrit per a generar 1 byte (8 bits), per la qual cosa requereix una operació de dos passos per a generar valors majors que 255.

```
// Do this for MSBFIRST serial
int data = 500;
// shift out highbyte
shiftOut(dataPin, clock, MSBFIRST, (data >> 8));
// shift out lowbyte
shiftOut(dataPin, clock, MSBFIRST, data);

// Or do this for LSBFIRST serial
int data = 500;
// shift out lowbyte
shiftOut(dataPin, clock, LSBFIRST, data);
// shift out highbyte
shiftOut(dataPin, clock, LSBFIRST, (data >> 8));
```

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
