---
títol: "random()"
descripció: ""
categoria: "Funcions"
subcategoria: "Numeros aleatoris"
---

# random()

### Descripcio

La funció aleatòria genera números pseudoaleatoris.

### Sintaxi

`random(max)`  
`random(min, max)`

### Paràmetres

`min`: límit inferior del valor aleatori, inclusivament (opcional).  
`max`: límit superior del valor aleatori, exclusiu.

### Devolucions

Un número aleatori entre min i max-1. Tipus de dada: long.

### Codi de exemple

El codi genera números aleatoris i els mostra.

```
long randNumber;

void setup()
{
  Serial.begin(9600);

  // si el pin d'entrada analògica 0 no està connectat,  
  // el soroll analògic aleatori farà que cada crida a randomSeed() genere
  // diferents números d'inicialització cada vegada que s'execute l'esbós.
  randomSeed(analogRead(0));
}

void loop() {
  // print a random number from 0 to 299
  randNumber ### random(300);
  Serial.println(randNumber);

  // print a random number from 10 to 19
  randNumber ### random(10, 20);
  Serial.println(randNumber);

  delay(50);
}
```

### Notes i Advertències

Si és important que una seqüència de valors generada per random() difereixi, en les execucions posteriors d'un esbós, utilitzeu randomSeed() per inicialitzar el generador de números aleatoris amb una entrada força aleatòria, com ara analogRead() en un pin no connectat.

Per contra, ocasionalment pot ser útil utilitzar seqüències pseudoaleatòries que es repeteixen exactament. Això es pot aconseguir cridant randomSeed() amb un nombre fix, abans d'iniciar la seqüència aleatòria.

El paràmetre màxim s'ha de triar segons el tipus de dades de la variable en què s'emmagatzema el valor. En qualsevol cas, el màxim absolut està lligat a la naturalesa llarga del valor generat (32 bits - 2.147.483.647). Establir el màxim a un valor més alt no generarà cap error durant la compilació, però durant l'execució de l’sketch els números generats no seran els esperats.

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
