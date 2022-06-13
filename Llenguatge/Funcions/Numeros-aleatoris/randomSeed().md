
| títol | descripció   | categoria  | subcategoria        |
| :---: | :----------: | :--------: | :-----------------: |
| randomSeed() | | Funcions | Nùmeros aleatoris |

# randomSeed()

### Descripcio

`randomSeed()` inicialitza el generador de números pseudoaleatoris, fent que s'iniciï en un punt arbitrari de la seva seqüència aleatòria. Aquesta seqüència, encara que molt llarga i aleatòria, és sempre la mateixa.

Si és important que una seqüència de valors generada per `random()` difereixi, en les execucions posteriors d'un esbós, utilitzeu `randomSeed()` per inicialitzar el generador de números aleatoris amb una entrada força aleatòria, com ara `analogRead()` en un pin no connectat.

Per contra, ocasionalment pot ser útil utilitzar seqüències pseudoaleatòries que es repeteixen exactament. Això es pot aconseguir cridant `randomSeed()` amb un nombre fix, abans d'iniciar la seqüència aleatòria.

### Sintaxi

* `randomSeed (seed)`

### Paràmetres

* `seed`: nombre per inicialitzar la seqüència pseudoaleatòria. Tipus de dades permesos: unsigned_long.

### Devolucions

Res

### Codi de exemple

El codi genera un número pseudoaleatori i envia el número generat al port sèrie.

```
long randNumber;

void setup()
{
  Serial.begin(9600);
  randomSeed(analogRead(0));
}

void loop()
{
  randNumber ### random(300);
  Serial.println(randNumber);
  delay(50);
}
```

### Veure també

* LLENGUATGE [Funcions](../Funcions.md)
