---
títol: [PROGMEM]
categoria: [ "Variables" ]
subcategoria: [ "Utilitats" ]
---

# PROGMEM

## Descripció

Emmagatzema les dades a la memòria flash (programa) en lloc de la SRAM. Hi ha una descripció dels diferents tipus de memòria disponibles en una placa Arduino.

La paraula clau `PROGMEM` és un modificador de variables, només s'ha d'utilitzar amb els tipus de dades definits a pgmspace.h. Li diu al compilador "posar aquesta informació a la memòria flaix", en lloc de la SRAM, on normalment aniria.

`PROGMEM` forma part de la biblioteca pgmspace.h. S'inclou automàticament a les versions modernes de l'IDE. Tanmateix, si utilitzeu una versió IDE inferior a 1.0 (2011), primer haureu d'incloure la biblioteca a la part superior del vostre croquis, com aquest:  
`#include <avr/pgmspace.h>` Tot i que PROGMEM es pot utilitzar en una sola variable, realment només val la pena l'enrenou si teniu un bloc de dades més gran que cal emmagatzemar, que normalment és més fàcil en una matriu (o una altra estructura de dades C++ més enllà de la nostra discussió actual).

L'ús de `PROGMEM` també és un procediment de dos passos. Després d'introduir les dades a la memòria Flash, es requereixen mètodes (funcions) especials, també definits a la biblioteca pgmspace.h, per tornar a llegir les dades de la memòria del programa a la SRAM, de manera que podem fer-hi alguna cosa útil.

## Sintaxi

`const dataType variableName[] PROGMEM = {data0, data1, data3…};`

Tingueu en compte que com que `PROGMEM` és un modificador de variables, no hi ha cap regla ferma i ràpida sobre on hauria d'anar, de manera que el compilador Arduino accepta totes les definicions següents, que també són sinònimes. Tanmateix, els experiments han indicat que, en diverses versions d'Arduino (que tenen a veure amb la versió GCC), `PROGMEM` pot funcionar en un lloc i no en un altre. L'exemple de "taula de cadenes" següent s'ha provat per funcionar amb Arduino 13. Les versions anteriors de l'IDE poden funcionar millor si s'inclou `PROGMEM` després del nom de la variable.

`const dataType variableName[] PROGMEM = {}; // utilitza aquest formulari`  
`const PROGMEM dataType variableName[] = {}; // o aquest`  
`const dataType PROGMEM variableName[] = {}; // no aquest`

## Paràmetres

`dataType`: tipus de dades permesos: qualsevol tipus de variable.  
`variableName`: el nom de la vostra matriu de dades.

## Exemple de codi

Els fragments de codi següents il·lustren com llegir i escriure caràcters sense signar (bytes) i int (2 bytes) a PROGMEM.

```
// save some unsigned ints
const PROGMEM uint16_t charSet[] = { 65000, 32796, 16843, 10, 11234};

// save some chars
const char signMessage[] PROGMEM = {"I AM PREDATOR,  UNSEEN COMBATANT. CREATED BY THE UNITED STATES DEPART"};

unsigned int displayInt;
char myChar;


void setup() {
  Serial.begin(9600);
  while (!Serial);  // wait for serial port to connect. Needed for native USB

  // put your setup code here, to run once:
  // read back a 2-byte int
  for (byte k = 0; k < 5; k++) {
    displayInt = pgm_read_word_near(charSet + k);
    Serial.println(displayInt);
  }
  Serial.println();

  // read back a char
  for (byte k = 0; k < strlen_P(signMessage); k++) {
    myChar = pgm_read_byte_near(signMessage + k);
    Serial.print(myChar);
  }

  Serial.println();
}

void loop() {
  // put your main code here, to run repeatedly:
}
Matrius de cadenes
Sovint és convenient quan es treballa amb grans quantitats de text, com ara un projecte amb una pantalla LCD, configurar una sèrie de cadenes. Com que les cadenes en si són matrius, aquest és en realitat un exemple de matriu bidimensional.
Aquestes solen ser estructures grans, de manera que sovint és desitjable posar-les a la memòria del programa. El codi següent il·lustra la idea.
/*
  PROGMEM string demo
  How to store a table of strings in program memory (flash),
  and retrieve them.

  Information summarized from:
  http://www.nongnu.org/avr-libc/user-manual/pgmspace.html

  Setting up a table (array) of strings in program memory is slightly complicated, but
  here is a good template to follow.

  Setting up the strings is a two-step process. First, define the strings.
*/

#include <avr/pgmspace.h>
const char string_0[] PROGMEM = "String 0"; // "String 0" etc are strings to store - change to suit.
const char string_1[] PROGMEM = "String 1";
const char string_2[] PROGMEM = "String 2";
const char string_3[] PROGMEM = "String 3";
const char string_4[] PROGMEM = "String 4";
const char string_5[] PROGMEM = "String 5";


// Then set up a table to refer to your strings.

const char *const string_table[] PROGMEM = {string_0, string_1, string_2, string_3, string_4, string_5};

char buffer[30];  // make sure this is large enough for the largest string it must hold

void setup() {
  Serial.begin(9600);
  while (!Serial);  // wait for serial port to connect. Needed for native USB
  Serial.println("OK");
}


void loop() {
  /* Using the string table in program memory requires the use of special functions to retrieve the data.
     The strcpy_P function copies a string from program space to a string in RAM ("buffer").
     Make sure your receiving string in RAM is large enough to hold whatever
     you are retrieving from program space. */


  for (int i = 0; i < 6; i++) {
    strcpy_P(buffer, (char *)pgm_read_word(&(string_table[i])));  // Necessary casts and dereferencing, just copy.
    Serial.println(buffer);
    delay(500);
  }
}
```

## Notes i advertències

Tingueu en compte que les variables s'han de definir globalment o bé amb la paraula clau estàtica, per tal de treballar amb `PROGMEM`.

El codi següent NO funcionarà quan estigui dins d'una funció:  
`const char long_str[] PROGMEM = "Hola, m'agradaria parlar-vos una mica de mi.\n";`  
El codi següent funcionarà, encara que estigui definit localment dins d'una funció:  
`const static char long_str[] PROGMEM = "Hola, m'agradaria parlar-vos una mica de mi.\n"`

## La macro F().

Quan una instrucció com:  
`Serial.print("Escriu alguna cosa al monitor sèrie");`  
s'utilitza, la cadena que s'ha d'imprimir es desa normalment a la memòria RAM. Si el vostre esbós imprimeix moltes coses al monitor sèrie, podeu omplir fàcilment la memòria RAM. Si teniu espai de memòria FLASH lliure, podeu indicar fàcilment que la cadena s'ha de desar a FLASH mitjançant la sintaxi:  
`Serial.print(F("Escriu alguna cosa al monitor sèrie que s'emmagatzema a FLASH"));`

## Vegeu també

EXEMPLE [Tipus de memòria disponibles en una placa Arduino](https://www.arduino.cc/playground/Learning/Memory)  
DEFINICIÓ [array](../Tipus-dades/array.md)  
DEFINICIÓ [string](../Tipus-dades/string.md)  
LLENGUATGE [Variables](../../Variables.md)
