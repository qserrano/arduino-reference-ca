---
títol: "serialEvent()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

| títol | descripció   | categoria  | subcategoria        |
| :---: | :----------: | :--------: | :-----------------: |
| serialEvent() | | Funcions | Comunicació |

# serialEvent()

### Descripció

Es cride quan hi ha dades disponibles. Use `Serial.read()` per a capturar aquestes dades.

### Sintaxi

```
void serialEvent() {
 //declaracions
}
```

Per a plaques amb ports sèrie addicionals (consulte la llista de ports serie disponibles per a cada placa en la pàgina principal de Serial):

```
void serialEvent1() {
 //declaracions
}

void serialEvent2() {
 //declaracions
}

void serialEvent3() {
 //declaracions
}
```

### Paràmetres

`declaracions`: qualsevol declaració vàlida

### Devolucions

Res

### Notes i Advertiments

`serialEvent()` no funciona en Leonardo, Micro o Yún.

`serialEvent()` i `serialEvent1()` no funcionen en les plaques Arduino SAMD

`serialEvent()`, `serialEvent1()`, `serialEvent2()` i `serialEvent3()` no funcionen en Arduino Due

##### Vegeu també

EXEMPLE [ReadASCIIString](https://www.arduino.cc/en/Tutorial/ReadASCIIString) (en anglés)  
EXEMPLE [ASCII Table](https://www.arduino.cc/en/Tutorial/ASCIITable) (en anglés)  
EXEMPLE [Dimmer](https://www.arduino.cc/en/Tutorial/Dimmer) (en anglés)  
EXEMPLE [Graph](https://www.arduino.cc/en/Tutorial/Graph) (en anglés)  
EXEMPLE [Physical Pixel](https://www.arduino.cc/en/Tutorial/PhysicalPixel) (en anglés)  
EXEMPLE [Serial Call Response](https://www.arduino.cc/en/Tutorial/SerialCallResponse) (en anglés)  
EXEMPLE [Serial Call Response ASCII](https://www.arduino.cc/en/Tutorial/SerialCallResponseASCII) (en anglés)  

LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
