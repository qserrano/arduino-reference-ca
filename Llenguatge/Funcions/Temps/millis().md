
| títol | descripció   | categoria  | subcategoria        |
| :---: | :----------: | :--------: | :-----------------: |
| millis() | | Funcions | Temps |

# millis()

### Descripció

Retorna el nombre de mil·lisegons passats dones que la placa Arduino va començar a executar el programa actual. Aquest nombre és desbordarà (tornarà a zero), després d'aproximadament 50 dies.

### Sintaxi

* `Time = millis()`

### Paràmetres

* Cap

### Devolucions

Nombre de mil·lisegons passats dones que el programa va començar. Tipus de dades: unsigned long.

### Exemple de codi

Aquest codi d'exemple imprimeix al port sèrie el nom de mil·lisegons passats dones que la placa Arduino va començar a executar el codi.

```
unsigned long myTime;

void setup() {
  Serial.begin(9600);
}
void loop() {
  Serial.print("Time: ");
  myTime = millis();

  Serial.println(myTime); // prints time since program started
  delay(1000);          // wait a second so as not to send massive amounts of data
}
```

### Notes i Advertiments

Tinga en compte que el valor de retorn per a `millis()` és de tipus unsigned long, poden ocórrer errors lògics si un programador intenta fer aritmètica amb tipus de dades més xicotetes com int. Fins i tot signed long pot trobar errors ja que el seu valor màxim és la meitat del de la seua contrapart sense signar.

### Veure també

* LLENGUATGE [Funcions](../Funcions.md)
