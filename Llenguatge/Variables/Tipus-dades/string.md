---
títol: "string"
categories: [ "Variables" ]
subcategories: [ "Tipus de dades" ]
---

# String

## Descripció

Les cadenes de text es poden representar de dues maneres. pot usar el tipus de dades `String`, que és part del nucli a partir de la versió 0019, o pot fer una cadena a partir d'una matriu de tipus `char` i acabar-la en zero. Aquesta pàgina descriu l'últim mètode. Per a obtindre més detalls sobre l'objecte `String`, que li brinda més funcionalitat a costa de més memòria, consulte la pàgina de l'objecte [String](./string-object.md).

## Sintaxi

Totes les següents són declaracions vàlides per a cadenes.

```
char Str1[15];
char Str2[8] = {'a', 'r', 'd', 'u', 'i', 'n', 'o'};
char Str3[8] = {'a', 'r', 'd', 'u', 'i', 'n', 'o', '\0'};
char Str4[] = "arduino";
char Str5[8] = "arduino";
char Str6[15] = "arduino";
```

**Possibilitats per a declarar cadenes**

- Declare una matriu de caràcters sense inicialitzar-la com en Str1
- Declare una matriu de caràcters (amb un caràcter addicional) i el compilador agregarà el caràcter nul requerit, com en Str2
- Agregue explícitament el caràcter nul, Str3
- Inicialitze amb una constant de cadena entre cometes; el compilador dimensionarà la matriu perquè s'ajuste a la constant de cadena i un caràcter nul de terminació, Str4
- Inicialitze la matriu amb una grandària explícita i una constant de cadena, Str5
- Inicialitze la matriu, deixant espai addicional per a una cadena més gran, Str6

**Terminació nul·la**

Generalment, les cadenes acaben amb un caràcter nul (codi ASCII 0). Això permet que les funcions (com a Serial.print()) indiquen on està el final d'una cadena. En cas contrari, continuarien llegint els bytes de memòria subsegüents que en realitat no formen part de la cadena.

Això significa que la seua cadena ha de tindre espai per a un caràcter més que el text que desitja que continga. És per això que Str2 i Str5 han de tindre huit caràcters, encara que "arduino" només té set: l'última posició s'ompli automàticament amb un caràcter nul. Str4 es dimensionarà automàticament a huit caràcters, un per al valor nul addicional. En Str3, hem inclòs explícitament el caràcter nul (escrit '\0') nosaltres mateixos.

Tinga en compte que és possible tindre una cadena sense un caràcter nul final (per exemple, si haguera especificat la longitud de Str2 com set en lloc de huit). Això trencarà la majoria de les funcions que usen cadenes, per la qual cosa no ha de fer-ho intencionalment. No obstant això, si nota que alguna cosa es comporta de manera estranya (operant en caràcters que no estan en la cadena), aquest podria ser el problema.

**¿Cometes simples o cometes dobles?**

Les cadenes sempre es defineixen dins de cometes dobles ("Abc") i els caràcters sempre es defineixen dins de cometes simples ("A").

**Dividir cadenes llargues**

Pot dividir cadenes llargues com aquesta:

```
char myString[] = "Aquesta es la primera linia"
" aquesta es la segona linia"
" etcetera";
```

**matrius de cadenes**

Sovint és convenient, quan es treballa amb grans quantitats de text, com un projecte amb una pantalla LCD, configurar una matriu de cadenes. Pel fet que les cadenes en si mateixes són matrius, aquest és en realitat un exemple d'una matriu bidimensional.

En el següent codi, l'asterisc després del caràcter de tipus de dades "char*" indica que es tracta d'una matriu de "punters". Tots els noms de matrius són en realitat punters, per la qual cosa això és necessari per a crear una matriu de matrius. Els punters són una de les parts més esotèriques de C ++ perquè els principiants entenguen, però no és necessari comprendre els punters detalladament per a usar-los de manera efectiva ací.

## Codi d’exemple

```
char *myStrings[] = {"This is string 1", "This is string 2", "This is string 3",
                     "This is string 4", "This is string 5", "This is string 6"
                    };

void setup() {
  Serial.begin(9600);
}

void loop() {
  for (int i = 0; i < 6; i++) {
    Serial.println(myStrings[i]);
    delay(500);
  }
}
```

## Veure també

LLENGUATGE [PROGMEM](../Utilitats/PROGMEM.md)  
LLENGUATGE [Variables](../../Variables.md)
