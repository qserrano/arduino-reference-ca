---
títol: "attachInterrupt()"
descripció: ""
categoria: "Funcions"
subcategoria: "Interrupcions externes"
---

# attachInterrupt()

### Descripció

### Pins digitals amb interrupcions

El primer paràmetre de `attachInterrupt()` és un número d'interrupció. Normalment, ha d'usar `digitalPinToInterrupt(pin)` per a traduir el pin digital real al número d'interrupció específic. Per exemple, si es connecta al pin 3, use `digitalPinToInterrupt(3)` com primer paràmetre per a `addedInterrupt()`.

| Board | Digital Pins Usable For Interrupts
| ----- | ------
| Uno, Nano, Mini, other 328-based | 2, 3
|Uno WiFi Rev.2, Nano Every | Tots els pins digitals
| Mega, Mega2560, MegaADK | 2, 3, 18, 19, 20, 21 (pins 20 i 21  no estan disponibles per les interrupcions mentre son utilitzats per a comunicació I2C)
| Micro, Leonardo, other 32u4-based | 0, 1, 2, 3, 7
| Zero | Tots els pins digitals, menys el 4
| MKR Family boards | 0, 1, 4, 5, 6, 7, 8, 9, A1, A2
| Nano 33 IoT | 2, 3, 9, 10, 11, 13, A1, A5, A7
| Nano 33 BLE, Nano 33 BLE Sense | Tots els pins
| Due | Tots els pins digitals
| 101 | Tots els pin digitals (només els pins 2, 5, 7, 8, 10, 11, 12, 13 funcionesn amb CHANGE)

### Notes i Advertiments

**Nota**

Dins de la funció adjunta, `delay()` no funcionarà i el valor retornat per `millis()` no s'incrementarà. Les dades en sèrie rebuts durant la funció poden perdre's. Ha de declarar com a volàtil qualsevol variable que modifique dins de la funció adjunta. Consulte la secció sobre ISR a continuació per a obtindre més informació.

**Us d'interrupcions**

Les interrupcions són útils per a fer que les coses succeïsquen automàticament en els programes de microcontroladors i poden ajudar a resoldre problemes de temporització. Les bones tasques per a usar una interrupció poden incloure llegir un codificador rotatori o monitorar l'entrada de l'usuari.

Si volguera assegurar-se que un programa sempre captara els polsos d'un codificador rotatori, perquè mai perda un pols, seria molt complicat escriure un programa per a fer qualsevol altra cosa, perquè el programa necessitaria sondejar constantment el sensor amb la finalitat de capturar els polsos quan es van produir. Altres sensors també tenen una dinàmica d'interfície similar, com intentar llegir un sensor de so que intenta captar un clic, o un sensor de ranura d'infrarojos (fotointerruptor) que intenta captar la caiguda d'una moneda. En totes aquestes situacions, l'ús d'una interrupció pot alliberar el microcontrolador per a fer un altre treball sense perdre l'entrada.

**Sobre les rutines de servei d'interrupció (ISR)**

Els ISR són tipus especials de funcions que tenen algunes limitacions úniques que la majoria de les altres funcions no tenen. Un ISR no pot tindre cap paràmetre i no hauria de retornar res.

En general, una ISR ha de ser el més curta i ràpida possible. Si el seu esbós usa múltiples ISR, només es pot executar un alhora, altres interrupcions s'executaran després que finalitze l'actual en un ordre que depén de la prioritat que tinguen. `millis()` es basa en les interrupcions per a comptar, per la qual cosa mai s'incrementarà dins d'un ISR. Atés que `delay()` requereix interrupcions per a funcionar, no funcionarà si es diu dins d'un ISR. `micros()` funciona inicialment però començarà a comportar-se de manera erràtica després de 1-2 ms. `delayMicroseconds()` no utilitza cap comptador, per la qual cosa funcionarà amb normalitat.

Normalment, les variables globals s'utilitzen per a passar dades entre un ISR i el programa principal. Per a assegurar-se que les variables compartides entre un ISR i el programa principal s'actualitzen correctament, declare-les com a volàtils.

Per a obtindre més informació sobre les interrupcions, consulte les [notes de Nick Gammon](http://gammon.com.au/interrupts).

### Sintaxi

`attachInterrupt(digitalPinToInterrupt(pin), ISR, mode)` (recomanat)  
`attachInterrupt(interrupt, ISR, mode)` (no recomanat)  
`attachInterrupt(pin, ISR, mode)` (No recomanat. A més, aquesta sintaxi només funciona amb Arduino SAMD Boards, Uno WiFi Rev2, Due, and 101.)

### Paràmetres

`interrupt` el número de la interrupció. Tipus de dades permeses: int.  
`pin` el número de pin d'Arduino.  
`ISR` l'ISR a cridar quan ocorre la interrupció; aquesta funció no ha de prendre paràmetres i no retornar res. Aquesta funció a vegades es denomina rutina de servei d'interrupció.  
`mode` defineix quan s'ha de disparar la interrupció. Quatre constants estan predefinides com a valors vàlids.
  - **LOW** per a activar la interrupció sempre que el pin estiga baix,
  - **CHANGE** per a activar la interrupció cada vegada que el pin canvie de valor
  - **RISING** per a disparar quan el pin va de baix a alt,
  - **FALLING** per a quan el pin va de major a menor.

Les targetes Due, Zero i MKR1000 també permeten:
- **HIGH** per a activar la interrupció sempre que el pin estiga alt.

### Devolucions

Res

### Codi d'exemple

```
const byte ledPin = 13;
const byte interruptPin = 2;
volatile byte state = LOW;

void setup()
{
  pinMode(ledPin, OUTPUT);
  pinMode(interruptPin, INPUT_PULLUP);
  attachInterrupt(digitalPinToInterrupt(interruptPin), blink, CHANGE);
}

void loop()
{
  digitalWrite(ledPin, state);
}

void blink()
{
  state = !state;
}
```

### Números d'interrupció

Normalment, ha d'usar `digitalPinToInterrupt(pin)`, en lloc de col·locar un número d'interrupció directament en el seu sketch. Els pins específics amb interrupcions i la seua assignació al nombre d'interrupcions varien per a cada tipus de placa. L'ús directe de números d'interrupció pot semblar simple, però pot causar problemes de compatibilitat quan el seu sketch s'executa en un tauler diferent.

No obstant això, els sketchs més antics sovint tenen números d'interrupció directes. Sovint s'usava el número 0 (per al pin digital 2) o el número 1 (per al pin digital 3). La següent taula mostra els pins d'interrupció disponibles en diverses plaques.

Tinga en compte que en la següent taula, els números d'interrupció es refereixen al número que es passarà a `attachInterrupt()`. Per raons històriques, aquesta numeració no sempre correspon directament a la numeració d'interrupcions en el xip ATmega (per exemple, int.0 correspon a INT4 en el xip ATmega2560).

| Board | int.0 | int.1 | int.2 | int.3 | int.4 | int.5
| ----- | ----- | ----- | ----- | ----- | ----- | -----
| Uno, Ethernet | 2 | 3 |  |  |  |  
| Mega2560 | 2 | 3 | 21 | 20 | 19 | 18
| 32u4 based (e.g Leonardo, Micro) | 3 | 2 | 0 | 1 | 7 |

Per a les plaques Un WiFiRev.2, Due, Zero, MKR Family i 101, el número d'interrupció = número de pin.

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
