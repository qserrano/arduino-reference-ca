---
títol: "#include"
descripció: ""
categoria: "Estructura"
subcategoria: "Sintaxi adicional"
---

# #include

### Descripció

`#include` s'usa per a incloure biblioteques externes en el seu esbós. Això li dona al programador accés a un gran grup de biblioteques C estàndard (grups de funcions prefabricades), i també biblioteques escrites especialment per a Arduino.

La pàgina de referència principal per a les biblioteques AVR C (AVR és una referència als xips Atmel en els quals es basa Arduino) és [ací](http://www.nongnu.org/avr-libc/user-manual/modules.html).

Tinga en compte que #include, similar a #define, no té terminador de punt i coma, i el compilador generarà missatges d'error críptics si agrega un.

### Sintaxi

`#include <LibraryFile.h>`  
`#include "LocalFile.h"`

### Paràmetres

`LibraryFile.h`: quan s'usa la sintaxi de claudàtors angulars, es buscarà l'arxiu en les rutes de les biblioteques.  
`LocalFile.h`: quan s'usa la sintaxi de cometes dobles, la carpeta de l'arxiu que usa la directiva `#include` es buscarà per a l'arxiu especificat, després les rutes de les biblioteques si no es troba en la ruta local. Utilitze aquesta sintaxi per a arxius d'encapçalat en la carpeta de l'esbós.

### Codi d'exemple

Aquest exemple inclou la biblioteca Servo perquè les seues funcions puguen usar-se per a controlar un motor Servo.

```
#include <Servo.h>

Servo myservo;  // crea un objecte servo per controlar un servo

void setup() {
  myservo.attach(9);  // connecta el servo al pin 9 a l'objecte servo
}

void loop() {
  for (int pos = 0; pos <= 180; pos += 1) { // passa de 0 graus a 180 graus
                                            // en passos d'1 grau
    myservo.write(pos);          // digues al servo que vagi a la posició a la variable 'pos'
    delay(15);                   // espera 15 ms perquè el servo arribi a la posició
  }
  for (int pos = 180; pos >= 0; pos -= 1) { // passa de 180 graus a 0 graus
    myservo.write(pos);          // digues al servo que vagi a la posició a la variable 'pos'
    delay(15);                   // espera 15 ms perquè el servo arribi a la posició
  }
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)  
