---
títol: for
descripció: ""
categoria: "Estructura"
subcategoria: "Control"
---

# for

### Descripció

La instrucció `for` s'usa per a repetir un bloc de declaracions entre claus. Normalment s'utilitza un comptador d'increments per a incrementar i acabar el bucle. La declaració `for` és útil per a qualsevol operació repetitiva i, sovint, s'usa en combinació amb matrius per a operar en col·leccions de dades/pins.

### Sintaxi

```
for (initialization; condition; increment) {
  // instruccions;
}
```

### Paràmetres

`initialization`: succeeix primer i exactament una vegada.  
`condition`: cada vegada que es passa pel cicle, es prova la condició; si és vertader, s'executa el bloc d'instrucció i l'increment, llavors la condició es prova novament. Quan la condició es torna falsa, el cicle acaba.  
`increment`: s'executa cada vegada que passa pel cicle quan la condició és vertadera.

### Codi d'exemple

```
// Atenuar un LED usant un pin PWM
int PWMpin = 10;  // LED en sèrie amb resistència de 470 ohm en el pin 10

void setup() {
  // no es necessita configuració
}

void loop() {
  for (int i = 0; i <= 255; i++) {
    analogWrite(PWMpin, i);
    delay(10);
  }
}
```

### Notes i Advertiments

El bucle for de C++ és molt més flexible que els bucles for que es troben en altres llenguatges informàtics, inclòs BASIC. Es pot ometre qualsevol dels tres elements de l'encapçalat o tots ells, encara que es requereixen els punts i coma. A més, les declaracions per a la inicialització, la condició i l'increment poden ser qualsevol declaració de C++ vàlida amb variables no relacionades i usar qualsevol tipus de dades de C++, inclosos els flotants. Aquests tipus de declaracions for inusuals poden proporcionar solucions a alguns problemes de programació rars.

Per exemple, usar una multiplicació en la línia d'increment generarà una progressió logarítmica:

```
for (int x = 2; x < 100; x = x * 1.5) {
  println(x);
}
```

Genera: 2,3,4,6,9,13,19,28,42,63,94

Un altre exemple, esvaïsca un LED cap amunt i cap avall amb un for loop:

```
void loop() {
  int x = 1;
  for (int i = 0; i > -1; i = i + x) {
    analogWrite(PWMpin, i);
    if (i == 255) {
      x = -1;  // canviar de direcció en el pic
    }
    delay(10);
  }
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
