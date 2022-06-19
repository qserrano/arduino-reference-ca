---
títol: "array"
categories: [ "Variables" ]
subcategories: [ "Tipus de dades" ]
---
# array

### Descripció

Una matriu és una col·lecció de variables a les quals s'accedeix amb un número d'índex. Els arrays en el llenguatge de programació C++ en els quals s'escriuen els esbossos d'Arduino poden ser complicats, però l'ús d’arrays simples és relativament senzill.

### Crear (declarar) una matriu

Tots els mètodes a continuació són formes vàlides de crear (declarar) una matriu.

```
int myInts[6];
int myPins[] = {2, 4, 8, 3, 6};
int mySensVals[5] = {2, 4, -8, 3, 2};
char missatge[6] = "hola";
```

Pot declarar una matriu sense inicialitzar-la com en myInts.

En myPins declarem una matriu sense triar explícitament una grandària. El compilador compta els elements i crea una matriu de la grandària adequada.

Finalment, pot inicialitzar i dimensionar la seua matriu, com en mySensVals. Tinga en compte que en declarar una matriu de tipus char, es requereix un element més que la seua inicialització per a contindre el caràcter nul requerit.

### Accés a una matriu

Les matrius estan indexades a zero, és a dir, en referència a la inicialització de la matriu anterior, el primer element de la matriu està en l'índex 0, per tant
`mySensVals[0] == 2, mySensVals[1] == 4, i així successivament.`

També significa que en una matriu amb deu elements, l'índex nou és l'últim element. Per això:
```
int myArray[10]={9, 3, 2, 4, 3, 2, 7, 8, 9, 11};
// myArray[9] conté 11
// myArray[10] no és vàlid i conté informació aleatòria (una altra direcció de memòria)
```
Per aquesta raó, ha d'anar amb compte en accedir a les matrius. Accedir més enllà del final d'una matriu (usant un número d'índex major que la grandària de matriu declarat - 1) és llegir de la memòria que està en ús per a altres fins. La lectura d'aquestes ubicacions probablement no farà molt, excepte generar dades no vàlides. Escriure en ubicacions de memòria aleatòries és definitivament una mala idea i, sovint, pot conduir a resultats desagradables, com a bloquejos o mal funcionament del programa. Això també pot ser un error difícil de rastrejar.

A diferència de BASIC o JAVA, el compilador de C++ no comprova si l'accés a la matriu està dins dels límits legals de la grandària de la matriu que ha declarat.

### Per a assignar un valor a una matriu:

`misValoresSensores[0] = 10;`

### Per a recuperar un valor d'una matriu:

`x = misValoresSensibles[4];`

### Matrius i bucles FOR

Les matrius sovint es manipulen dins dels bucles, on el comptador de bucles s'usa com a índex per a cada element de la matriu. Per exemple, per a imprimir els elements d'una matriu en el port serie, podria fer alguna cosa com això:
```
for (byte i = 0; i < 5; i = i + 1) {
 Serial.println(myPins[i]);
}
```

### Codi d'exemple

Per a veure un programa complet que demostra l'ús d'arranjaments, veja el ([exemple de Knight Rider](http://www.arduino.cc/en/Tutorial/KnightRider)) dels ([Tutorials](http://www.arduino.cc/en/Main/LearnArduino)).

### Veure també

LLENGUATGE [PROGMEM](https://www.arduino.cc/reference/en/language/variables/utilities/progmem)  
LLENGUATGE [Variables](../../Variables.md)
