---
títol: "pinMode()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Digitals"
---

# pinMode()

### Descripció

Configura el pin especificat perquè es comporte com una entrada o una eixida. Consulte la pàgina Pins digitals per a obtindre detalls sobre la funcionalitat dels pins.
A partir d'Arduino 1.0.1, és possible habilitar les resistències pullup internes amb el mode INPUT_PULLUP. A més, el mode INPUT deshabilita explícitament els pullups interns.

### Sintaxi

`pinMode(pin, mode)`

### Paràmetres

`pin`: el número de pin d'Arduino per a establir el mode  
`mode`: INPUT, OUTPUT o INPUT_PULLUP. Consulte la pàgina Pins digitals per a obtindre una descripció més completa de la funcionalitat.  

### Devolucions

Res

### Codi d'exemple

El codi defineix el pin digital 13 com EIXIDA i l'alterna HIGH i LOW

```
void setup ()
{
 pinMode(13, OUTPUT); // estableix el pin digital 13 com a eixida
}

void loop ()
{
 digitalWrite (13, HIGH); // activa el pin digital 13
 delay (1000); // espera un segon
 digitalWrite (13, LOW); // desactiva el pin digital 13
 delay (1000); // espera un segon
}
```

### Notes i Advertiments

Els pins d'entrada analògica es poden usar com a pins digitals, denominats A0, A1, etc.

### Veure també

EXEMPLE [Descripció dels pins digitals (en anglés)](http://arduino.cc/en/Tutorial/DigitalPins)  
LLENGUATGE [Funcions](../../Funcions.md)
