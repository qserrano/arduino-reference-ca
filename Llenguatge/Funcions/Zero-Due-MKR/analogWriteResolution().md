---
títol: "analogWriteResolution()"
descripció: ""
categoria: "Funcions"
subcategoria: "USB"
---

# analogWriteResolution()

### Descripció

`analogWriteResolution()` és una extensió de l'API analògica per a Arduino Due.

`analogWriteResolution()` estableix la resolució de la funció `analogWrite()`. Té un valor predeterminat de 8 bits (valors entre 0 i 255)
per a compatibilitat amb versions anteriors de plaques basades en AVR.

El Due té les següents capacitats de maquinari:
* 12 pins que per defecte són PWM de 8 bits, com les plaques basades en AVR. Aquests es poden canviar a una resolució de 12 bits.
* 2 pins amb DAC de 12 bits (convertidor de digital a analògic)

En configurar la resolució d'escriptura en 12, pot usar `analogWrite()` amb valors entre 0 i 4095 per a explotar la resolució completa de DAC o per
a configurar el senyal PWM sense canviar.

El Zero té les següents capacitats de maquinari:
* 10 pins que per defecte són PWM de 8 bits, com les plaques basades en AVR. Aquests es poden canviar a una resolució de 12 bits.
* 1 pin amb DAC de 10 bits (convertidor de digital a analògic).

En establir la resolució d'escriptura en 10, pot usar `analogWrite()` amb valors entre 0 i 1023 per a aprofitar la resolució DAC completa

La família de plaques MKR té les següents capacitats de maquinari:
* 4 pins que per defecte són PWM de 8 bits, com les plaques basades en AVR. Aquests es poden canviar de 8 (predeterminat) a 12 bits de resolució.
* 1 pin amb DAC de 10 bits (convertidor de digital a analògic)

En establir la resolució d'escriptura en 12 bits, pot usar `analogWrite()` amb valors entre 0 i 4095 per a senyals PWM; configure 10 bits en el pin DAC
per a explotar la resolució DAC completa de 1024 valors.

### Sintaxi

`analogWriteResolution(bits)`

### Paràmetres

`bits`: determina la resolució (en bits) dels valors utilitzats en la funció `analogWrite()`. El valor pot oscil·lar entre 1 i 32.  
Si tria una resolució superior o inferior a les capacitats de maquinari de la seua placa, el valor utilitzat en `analogWrite()` es truncarà si és massa alt o s'emplenarà amb zeros si és massa baix. Consulte la nota a continuació per a obtindre més detalls.

### Devolucions

Res

### Codi d'exemple

```
void setup()
{
  // open a serial connection
  Serial.begin(9600);
  // make our digital pin an output
  pinMode(11, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(13, OUTPUT);
}

void loop()
{
  // read the input on A0 and map it to a PWM pin
  // with an attached LED
  int sensorVal = analogRead(A0);
  Serial.print("Analog Read) : ");
  Serial.print(sensorVal);

  // the default PWM resolution
  analogWriteResolution(8);
  analogWrite(11, map(sensorVal, 0, 1023, 0, 255));
  Serial.print(" , 8-bit PWM value : ");
  Serial.print(map(sensorVal, 0, 1023, 0, 255));

  // change the PWM resolution to 12 bits
  // the full 12 bit resolution is only supported
  // on the Due
  analogWriteResolution(12);
  analogWrite(12, map(sensorVal, 0, 1023, 0, 4095));
  Serial.print(" , 12-bit PWM value : ");
  Serial.print(map(sensorVal, 0, 1023, 0, 4095));

  // change the PWM resolution to 4 bits
  analogWriteResolution(4);
  analogWrite(13, map(sensorVal, 0, 1023, 0, 15));
  Serial.print(", 4-bit PWM value : ");
  Serial.println(map(sensorVal, 0, 1023, 0, 15));

  delay(5);
}
```

### Notes i Advertiments

Si estableix el valor `analogWriteResolution()` en un valor superior a les capacitats de la seua placa, l'Arduino descartarà els bits addicionals.
Per exemple: en usar Due amb analogWriteResolution(16) en un pin DAC de 12 bits, només s'usaran els primers 12 bits dels valors passats a `analogWrite()`
i es descartaran els últims 4 bits.
Si estableix el valor `analogWriteResolution()` en un valor inferior a les capacitats de la seua placa, els bits que manca s'emplenaran amb zeros per a omplir la grandària requerida de maquinari. Per exemple: usant Due amb analogWriteResolution(8) en un pin DAC de 12 bits, arduino agregarà 4 bits zero al valor de 8 bits usat en `analogWrite()` per a obtindre els 12 bits requerits.

### Veure també

LLENGUATGE [analogWrite()](../ES-Analogiques/analogWrite().md)  
LLENGUATGE [analogRead()](../ES-Analogiques/analogRead().md)  
LLENGUATGE [map()](../Matematiques/map().md)  
EXEMPLE    [Descripció dels pins d'entrada analògica (en anglés)](http://arduino.cc/en/Tutorial/AnalogInputPins)  
LLENGUATGE [Funcions](../../Funcions.md)
