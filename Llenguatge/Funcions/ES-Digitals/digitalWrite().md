---
títol: "digitalWrite()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Digitals"
---

# digitalWrite()

### Descripció

Escriu un valor HIGH o LOW en un pin digital.

Si el pin ha sigut configurat com a EIXIDA amb pinMode(), el seu voltatge s'establirà en el valor corresponent: 5V (o 3.3V en plaques de 3.3V) per a HIGH, 0V (terra) per a LOW.

Si el pin està configurat com a ENTRADA, digitalWrite() habilitarà (HIGH) o deshabilitarà (LOW) el pull-up intern en el pin d'entrada. Es recomana establir pinMode() en INPUT_PULLUP per a habilitar la resistència pull-up interna. Consulte el tutorial Pins digitals per a obtindre més informació.

Si no configura pinMode() en OUTPUT i connecta un LED a un pin, quan cride a digitalWrite (HIGH), el LED pot aparéixer tènue. Sense establir explícitament pinMode(), digitalWrite() haurà habilitat la resistència pull-up interna, que actua com una gran resistència limitadora de corrent.

### Sintaxi

`digitalWrite(pin, value)`

### Paràmetres

`pin`: el número de pin d'Arduino.  
`value`: HIGH o LOW.  

### Devolucions

Res

### Codi d'exemple

El codi converteix el pin digital 13 en una EIXIDA i el canvia alternant entre HIGH i LOW a un ritme d'un segon.

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

Els pins d'entrada analògica es poden usar com a pins digitals, denominats A0, A1, etc. L'excepció són els pins A6 i A7 d'Arduino Nano, Pro Mini i Mini, que només es poden usar com a entrades analògiques.

### Veure també

EXEMPLE [Descripció dels pins digitals (en anglés)](http://arduino.cc/en/Tutorial/DigitalPins)  
LLENGUATGE [Funcions](../../Funcions.md)
