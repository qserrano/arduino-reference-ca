---
títol: [volatile]
categoria: [ "Variables" ]
subcategoria: [ "Abast de variables" ]
---

# volatile

## Descripció

`volatile` és una paraula clau coneguda com a qualificador de variable, normalment s'utilitza abans del tipus de dades d'una variable, per modificar la forma en què el compilador i el programa posterior tracten la variable.

Declarar una variable volàtil és una directiva per al compilador. El compilador és un programari que tradueix el vostre codi C/C++ al codi màquina, que són les instruccions reals per al xip Atmega a l'Arduino.

Concretament, indica que el compilador carregui la variable des de la memòria RAM i no des d'un registre d'emmagatzematge, que és una ubicació de memòria temporal on s'emmagatzemen i manipulen les variables del programa. En determinades condicions, el valor d'una variable emmagatzemada als registres pot ser inexacte.

Una variable s'ha de declarar volàtil sempre que el seu valor es pugui canviar per alguna cosa fora del control de la secció de codi en què apareix, com ara un fil que s'executa simultàniament. A l'Arduino, l'únic lloc on és probable que això passi és a les seccions de codi associades a interrupcions, anomenades rutina de servei d'interrupcions.

## volàtils int o long

Si la variable volàtil és més gran que un byte (per exemple, un int de 16 bits o un de 32 bits de llarg), el microcontrolador no pot llegir-lo en un sol pas, perquè és un microcontrolador de 8 bits. Això vol dir que, mentre que la secció de codi principal (per exemple, el vostre bucle) llegeix els primers 8 bits de la variable, la interrupció ja pot canviar els segons 8 bits. Això produirà valors aleatoris per a la variable.

**Remei:**  
Mentre es llegeix la variable, les interrupcions s'han de desactivar, de manera que no es puguin embrutar amb els bits mentre es llegeixen. Hi ha diverses maneres de fer-ho:
- LLENGUATGE noInterrupts
- utilitzeu la macro ATOMIC_BLOCK. Les operacions atòmiques són operacions de MCU individuals: la unitat més petita possible.

## Exemple de codi

El modificador volàtil garanteix que els canvis a la variable d'estat siguin visibles immediatament a loop(). Sense el modificador volàtil, la variable d'estat es pot carregar en un registre en entrar a la funció i no s'actualitzaria més fins que acabi la funció.

```
// Parpelleja el LED durant 1 s si l'entrada ha canviat
// al segon anterior.

volatile byte changed = 0;

void setup() {
  pinMode(LED_BUILTIN, SORTIDA);
  attachInterrupt(digitalPinToInterrupt(2), alterna, CANVI);
}

void loop() {
  if (changed == 1) {
    // S'ha cridat a toggle() des de les interrupcions!

    // Inicialitzar changed a 0
    changed = 0;

    // LED intermitent durant 200 ms
    digitalWrite(LED_BUILTIN, HIGH);
    retard (200);
    digitalWrite(LED_BUILTIN, LOW);
  }
}

void toggle () {
  changed = 1;
}
```

Per accedir a una variable amb una mida superior a la del bus de dades de 8 bits del microcontrolador, utilitzeu la macro ATOMIC_BLOCK. La macro assegura que la variable es llegeix en una operació atòmica, és a dir, el seu contingut no es pot alterar mentre es llegeix.

```
#include <util/atomic.h> // aquesta biblioteca inclou la macro ATOMIC_BLOCK.
volatile int input_from_interrupt;

// En algun lloc del codi, p.e. bucle interior ()
  ATOMIC_BLOCK(ATOMIC_RESTORESTATE) {
    // codi amb interrupcions bloquejades (les operacions atòmiques consecutives no s'interrompran)
    int result = input_from_interrupt;
  }
```

## Vegeu també

LLENGUATGE [attachInterrupt()](../../Funcions/Interrupcions-externes/attachInterrupt().md)  
LLENGUATGE [Variables](../../Variables.md)  

