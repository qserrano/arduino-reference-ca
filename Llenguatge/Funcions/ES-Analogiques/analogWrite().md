---
títol: "analogWrite()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Analogiques"
---

# analogWrite()

### Descripció

Escriu un valor analògic (ona PWM) en un pin. Es pot usar per a encendre un LED amb diferents lluentors o impulsar un motor a diverses velocitats.

Després de cridar a `analogWrite()`, el pin generarà una ona rectangular constant del cicle de treball especificat fins a la pròxima crida a `analogWrite()` (o una crida a `digitalRead()` o `digitalWrite()`) en el mateix pin.

Placa | Pins PWM | Freqüència PWM
--- | --- | ---
Uno, Nano, Mini | 3, 5, 6, 9, 10, 11 | 490 Hz (pins 5 i 6: 980 Hz)
Mega | 2 - 13, 44 - 46 | 490 Hz (pins 4 i 13: 980 Hz)
Leonardo, Micro, Yún | 3, 5, 6, 9, 10, 11, 13 | 490 Hz (pins 3 i 11: 980 Hz)
Uno WiFi Rev2, Nano Every | 3, 5, 6, 9, 10 | 976 Hz
MKR boards * | 0 - 8, 10, A3, A4 | 732 Hz
MKR1000 WiFi * | 0 - 8, 10, 11, A3, A4 | 732 Hz
Zero * | 3 - 13, A0, A1 | 732 Hz
Nano 33 IoT * | 2, 3, 5, 6, 9 - 12, A2, A3, A5 | 732 Hz
Nano 33 BLE/BLE Sense | 1 - 13, A0 - A7 | 500 Hz
Due ** | 2-13 | 1000 Hz
101 | 3, 5, 6, 9 | pins 3 i 9: 490 Hz, pins 5 i 6: 980 Hz

\* A més de les capacitats de PWM en els pins indicats anteriorment, les plaques MKR, Nano 33 IoT i Zero tenen eixida analògica vertadera quan s'usa
analogWrite() en el pin DAC0 (A0).

** A més de les capacitats de PWM en els pins esmentats anteriorment, Due té una eixida analògica vertadera quan s'usa analogWrite() en els pins DAC0 i DAC1.

No necessita cridar a pinMode() per a configurar el pin com a eixida abans de cridar a analogWrite().

La funció analogWrite no té res a veure amb els pins analògics o la funció analogRead.

### Sintaxi

`analogWrite(pin, value)`

### Paràmetres

`pin`: el pin d'Arduino per a escriure. Tipus de dades permeses: int.  
`value`: el cicle de treball: entre 0 (sempre apagat) i 255 (sempre encés). Tipus de dades permeses: int.

### Devolucions

Res

### Codi d'exemple

Estableix l'eixida al LED proporcional al valor llegit del potenciòmetre.

```
int ledPin = 9;      // LED connectat al pin digital 9
int analogPin = 3;   // pot. Connectat al pin analogic 3
int val = 0;         // variable per guardar el valor llegit

void setup()
{
  pinMode(ledPin, OUTPUT);  // estableix ledPin com eixida
}

void loop()
{
  val = analogRead(analogPin);  // llig el pin d’entrada
  analogWrite(ledPin, val / 4); // els valors llegits van de 0 to 1023,
                                // els valors escrits de 0 to 255
}
```

### Notes i Advertiments

Les eixides PWM generades en els pins 5 i 6 tindran cicles de treball més alts de l'esperat. Això es deu a les interaccions amb les funcions `millis()` i `delay()`, que comparteixen el mateix temporitzador intern que s'usa per a generar aqueixes eixides PWM. Això es notarà principalment en configuracions de cicle de treball baix (per exemple, 0 - 10) i pot resultar en un valor de 0 que no apague completament l'eixida en els pins 5 i 6.

### Veure també

LLENGUAGE [analogWriteResolution() (en anglés)](https://www.arduino.cc/reference/en/language/functions/zero-due-mkr-family/analogwriteresolution)  
DEFINICIÓ [PWM (en anglés)](http://arduino.cc/en/Tutorial/PWM)  
EXEMPLE  [ Blink (en anglés)](http://arduino.cc/en/Tutorial/Blink)  
LLENGUATGE [Funcions](../../Funcions.md)
