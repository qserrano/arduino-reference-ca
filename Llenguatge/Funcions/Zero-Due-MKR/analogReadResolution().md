---
títol: "analogReadResolution()"
descripció: ""
categoria: "Funcions"
subcategoria: "Zero, DUE, MKR"
---

# analogReadResolution()

### Descripció

`analogReadResolution()` és una extensió de l'API analògica per a la família Zero, Due, MKR, Nano 33 (BLE i IoT) i Portenta.

Estableix la mesure (en bits) del valor retornat per `analogRead()`. Per defecte, és de 10 bits (retorna valors entre 0 i 1023) per a la compatibilitat amb els plaques basades en AVR.

Les plaques Zero, Due, MKR i Nano 33 (BLE i IoT) tenen capacitats ADC (Analog-to-Digital Converter) de 12 bits als quals és pot accedir canviant la resolució a 12. Això retornarà valors d'`analogRead()` entre 0 i 4095.

El Portenta H7 te un ADC de 16 bits, que permetrà valors entre 0 i 65535.

### Sintaxi

`analogReadResolution(bits)`

### Paràmetres

`bits`: determina la resolució (en bits) del valor retornat per la funció analogRead(). Podeu establir-ho entre 1 i 32. Podeu establir resolucions superiors als 12 o 16 bits admesos, però els valors retornats per analogRead() patiran aproximació.   Consulteu la nota a continuació per obtenir més informació.

### Devolucions

Res

### Exemple de codi

El codi mostra com utilitzar l'ADC amb diferents resolucions.

```
void setup()
{
  // obre una connexió serie
  Serial.begin(9600);
}

void loop()
{
  // llig l’entrada A0 amb la resolució per defecte (10 bits)
  // i la envia al monitor serie
  analogReadResolution(10);
  Serial.print("ADC 10-bit (default) : ");
  Serial.print(analogRead(A0));

  // canvia la resolució a 12 bits i llig A0
  analogReadResolution(12);
  Serial.print(", 12-bit : ");
  Serial.print(analogRead(A0));

  // canvia la resolució a 16 bits i llig A0
  analogReadResolution(16);
  Serial.print(", 16-bit : ");
  Serial.print(analogRead(A0));

  // canvia la resolució a 8 bits i llig A0
  analogReadResolution(8);
  Serial.print(", 8-bit : ");
  Serial.println(analogRead(A0));

  // un xicotet retard per no saturar el monitor serie
  delay(100);
}
```

### Notes i Advertiments

Si estableix el valor `analogReadResolution()` en un valor superior a les capacitats de la seua placa, l'Arduino només informarà la seua resolució més alta, emplenant els bits addicionals amb zeros.

Per exemple: usar Due amb `analogReadResolution(16)` li donarà un número aproximat de 16 bits amb els primers 12 bits que contenen la lectura real d'ADC i els últims 4 bits emplenats amb zeros.

Si estableix el valor `analogReadResolution()` en un valor inferior a les capacitats de la seua placa, els bits extra menys significatius llegits de l'ADC es descartaran.

L'ús d'una resolució de 16 bits (o qualsevol resolució superior a les capacitats reals del maquinari) li permet escriure sketchs que manegen automàticament dispositius amb un ADC de major resolució quan estiguen disponibles en plaques futures sense canviar una línia de codi.

### Veure també

EXEMPLE [Descripció dels pins d'entrada analògica (en anglés)](http://arduino.cc/en/Tutorial/AnalogInputPins)  
LLENGUAGE [analogRead()](Llenguatge/Funcions/ES-Analogiques/analogRead().md)  
LLENGUATGE [Funcions](../../Funcions.md)
