---
títol: Constants
categories: [ "Variables" ]
subcategories: [ "Constants" ]
---

# Constants

## Descripció

Les constants són expressions predefinides en el llenguatge Arduino. S'utilitzen per facilitar la lectura dels programes.

Classifiquem les constants en grups:
- true/false
- HIGH/LOW
- INPUT, INPUT_PULLUP, OUTPUT
- LED_BUILTIN

## Definició de nivells lògics: true i false (constants booleanes)

Hi ha dues constants que s'utilitzen per a representar la veritat i la falsedat en el llenguatge Arduino: true i false.

### false

false és el més fàcil de definir dels dos. false es defineix com 0 (zero).

### true

Sovint es diu que true es defineix com 1, la qual cosa és correcte, però true té una definició més àmplia. Qualsevol nombre enter que no siga zero és vertader, en un sentit booleà. Llavors, -1, 2 i -200 també es defineixen com a vertaders en un sentit booleà.

Tinga en compte que les constants vertader i fals s'escriuen en minúscules a diferència d'ALT, BAIX, ENTRADA i EIXIDA.

## Definició de nivells de pins: HIGH i LOW

Al llegir o escriure en un pin digital, només hi ha dos valors possibles que un pin pot prendre/establir: HIGH i LOW.

### HIGH

El significat de HIGH (en referència a un pin) és una cosa diferent depenent de si un pin està configurat com a ENTRADA o EIXIDA. Quan un pin es configura com a ENTRADA amb `pinMode()` i es llig amb `digitalRead()`, l'Arduino (ATmega) informarà HIGH si:
- un voltatge major a 3.0V és present en el pin (plagues de 5V)
- un voltatge superior a 2,0 V és present en el pin (plaques de 3,3 V)

Un pin també pot configurar-se com una ENTRADA amb `pinMode()` i, posteriorment, establir-se a HIGH amb `digitalWrite()`. Això habilitarà les resistències pull-up internes de 20K, que elevaran el pin d'entrada a una lectura HIGH llevat que un circuit extern el baixe. Això es pot fer alternativament passant INPUT_PULLUP com a argument a la funció `pinMode()`, com s'explica amb més detall en la secció "Definició dels modes de pins digitals: INPUT, INPUT_PULLUP i OUTPUT" més endavant.

Quan un pin es configura en EIXIDA amb `pinMode()` i s'estableix a HIGH amb `digitalWrite()`, el pin està en:
- 5 volts (taulers de 5V)
- 3,3 volts (plaques de 3,3 V)

En aquest estat pot generar corrent, p.e. encén un LED que està connectat a terra a través d'una resistència en sèrie.

### LOW

El significat de LOW també té un significat diferent depenent de si un pin està configurat en ENTRADA o EIXIDA. Quan un pin es configura com a ENTRADA amb `pinMode()` i es llig amb `digitalRead()`, l'Arduino (ATmega) informarà LOW si:
- un voltatge inferior a 1,5 V és present en el pin (taulers de 5 V)
- hi ha un voltatge inferior a 1,0 V (aprox.) en el pin (plaques de 3,3 V)

Quan un pin es configura en EIXIDA amb `pinMode()` i s'estableix en LOW amb `digitalWrite()` , el pin està a 0 volts (tant en les plaques de 5 V com de 3,3 V). En aquest estat pot absorbir corrent, p.e. encén un LED que està connectat a través d'una resistència en sèrie a +5 volts (o +3,3 volts).

## Definició de modos de pins digitals: INPUT, INPUT_PULLUP i OUTPUT

Els pins digitals es poden usar com a INPUT, INPUT_PULLUP o OUTPUT. Canviar un pin amb pinMode() canvia el comportament elèctric del pin.

### Pins configurats com a INPUT

Es diu que els pins Arduino (ATmega) configurats com a INPUT amb pinMode() estan en un estat d'alta impedància. Els pins configurats com a INPUT fan demandes extremadament xicotetes en el circuit que estan mostrejant, equivalents a una resistència en sèrie de 100 megaohms enfront del pin. Això els fa útils per a llegir un sensor.

Si té el seu pin configurat com a INPUT i està llegint un interruptor, quan l'interruptor està en estat obert, el pin d'entrada estarà "surant", la qual cosa donarà resultats impredictibles. Per a assegurar una lectura adequada quan l'interruptor està obert, s'ha d'usar una resistència pull-up o pull-down. El propòsit d'aquesta resistència és portar el pin a un estat conegut quan l'interruptor està obert. En general, es tria una resistència de 10 K ohms, ja que és un valor prou baix per a evitar una entrada flotant i, al mateix temps, un valor prou alt per a no consumir massa corrent quan l'interruptor està tancat. Consulte el tutorial Digital Read Serial per a obtindre més informació.
- Si s'usa una resistència pull-down, el pin d'entrada serà LOW quan l'interruptor estiga obert i HIGH quan l'interruptor estiga tancat.
- Si s'usa una resistència pull-up, el pin d'entrada serà HIGH quan l'interruptor estiga obert i LOW quan l'interruptor estiga tancat.

### Pins configurats com a INPUT_PULLUP

El microcontrolador ATmega en l'Arduino té resistències pull-up internes (resistències que es connecten internament a l'alimentació) a les quals pot accedir. Si prefereix usar aquests en lloc de resistències pull-up externes, pot usar l'argument INPUT_PULLUP en pinMode().

Consulte el tutorial Input Pullup Serial per a veure un exemple d'això en ús.

Els pins configurats com a entrades amb INPUT o INPUT_PULLUP poden danyar-se o destruir-se si es connecten a voltatges per baix de zero (voltatges negatius) o per damunt de l'alimentació positiva (5V o 3V).

### Pins configurats com a OUTPUT

Es diu que els pins configurats com a OUTPUT amb pinMode() estan en un estat de baixa impedància. Això significa que poden proporcionar una quantitat substancial de corrent a altres circuits. Els pins ATmega poden generar (proporcionar corrent) o afonar (absorbir corrent) fins a 40 mA. (miliampers) de corrent a altres dispositius/circuits. Això els fa útils per a alimentar LEDs perquè els LED solen usar menys de 40 mA.. Les càrregues superiors a 40 mA. (per exemple, motors) requeriran un transistor o un altre circuit d'interfície.

Els pins configurats com a eixides poden danyar-se o destruir-se si estan connectats a terra o als borns d'alimentació positius.

## Definició d'integrats: LED_BUILTIN

La majoria de plaques Arduino tenen un pin connectat a un LED integrat en sèrie amb una resistència. La constant LED_BUILTIN és el número del pin al qual està connectat el LED integrat. La majoria de plaques tenen aquest LED connectat al pin digital 13.

## Vegeu també

LLENGUATGE [Variables](../../Variables.md)  

