---
títol: "Wire.setWireTimeout()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Wire"
---

# setWireTimeout()

### Descripció

Estableix el temps d'espera per a les transmissions per cable en mode mestre.

**Nota**: aquests temps d'espera gairebé sempre són una indicació d'un problema subjacent, com ara un mal comportament dels dispositius, soroll, blindatge insuficient o altres problemes elèctrics. Aquests temps d'espera evitaran que el vostre esbós es bloquegi, però no resoldran aquests problemes. En aquestes situacions sovint hi haurà (també) corrupció de dades que no es tradueix en un temps d'espera o un altre error i no es detecta. Així, quan es produeix un temps d'espera, és probable que algunes dades llegides o escrites anteriorment també estiguin malmeses. És possible que calguin mesures addicionals per detectar aquests problemes de manera més fiable (p. ex., sumes de comprovació o llegir els valors escrits) i recuperar-los (p. ex., restabliment complet del sistema). Aquest temps d'espera i aquestes mesures addicionals s'han de veure com una última línia de defensa, quan sigui possible, la causa subjacent s'hauria de solucionar.

### Sintaxi

`Wire.setWireTimeout(timeout, reset_on_timeout)`  
`Wire.setWireTimeout()`  

### Paràmetres

`timeout`: temps d'espera en microsegons, si és zero, la comprovació del temps d'espera està desactivada  
`reset_on_timeout`: si és cert, el maquinari Wire es reiniciarà automàticament en el temps d'espera  

Quan es crida aquesta funció sense paràmetres, es configura un temps d'espera predeterminat que hauria de ser suficient per evitar bloquejos en una configuració típica d'un sol mestre.

### Devolucions

Cap. 

### Exemple de codi

```
#include <Wire.h>

void setup() {
  Wire.begin(); // join i2c bus (address optional for master)
  #if defined(WIRE_HAS_TIMEOUT)
    Wire.setWireTimeout(3000 /* us */, true /* reset_on_timeout */);
  #endif
}

byte x = 0;

void loop() {
  /* First, send a command to the other device */
  Wire.beginTransmission(8); // transmit to device #8
  Wire.write(123);           // send command
  byte error = Wire.endTransmission(); // run transaction
  if (error) {
    Serial.println("Error occured when writing");
    if (error == 5)
      Serial.println("It was a timeout");
  }

  delay(100);

  /* Then, read the result */
  #if defined(WIRE_HAS_TIMEOUT)
  Wire.clearWireTimeoutFlag();
  #endif
  byte len = Wire.requestFrom(8, 1); // request 1 byte from device #8
  if (len == 0) {
    Serial.println("Error occured when reading");
    #if defined(WIRE_HAS_TIMEOUT)
    if (Wire.getWireTimeoutFlag())
      Serial.println("It was a timeout");
    #endif
  }

  delay(100);
}
```

### Notes i advertències

La forma en què s'implementa aquest temps d'espera pot variar entre diferents plataformes, però normalment s'activa una condició de temps d'espera quan s'espera que (alguna part de) la transacció es completi (per exemple, esperant que l'autobús torni a estar disponible, esperant un bit ACK o potser esperant. perquè es completi tota la transacció).

Quan es produeix aquesta condició de temps d'espera, la transacció s'avorta i `endTransmission()` o `requestFrom()` retornarà un codi d'error o zero bytes respectivament. Tot i que això no resoldrà el problema del bus per si mateix (és a dir, no elimina un curtcircuit), almenys evitarà el bloqueig potencialment indefinida i permetrà que el vostre programari detecti i potser resolgui aquesta condició.

Si reset_on_timeout s'ha establert com a true i la plataforma ho admet, també es restableix el maquinari Wire, cosa que pot ajudar a esborrar qualsevol estat incorrecte dins del mòdul de maquinari Wire. Per exemple, a la plataforma AVR, això pot ser necessari per reiniciar les comunicacions després d'un temps d'espera induït pel soroll.

Quan s'activa un temps d'espera, s'estableix una marca que es pot consultar amb `getWireTimeoutFlag()` i que s'ha d'esborrar manualment amb `clearWireTimeoutFlag()` (i també s'esborra quan es crida a `setWireTimeout()`).

Tingueu en compte que aquest temps d'espera també es pot activar mentre s'espera l'estirament del rellotge o que un segon mestre completi la seva transacció. Així que assegureu-vos d'adaptar el temps d'espera per adaptar-se a aquests casos si cal. Un temps d'espera típic seria de 25 ms (que és l'estirament màxim del rellotge que permet el protocol SMBus), però normalment també funcionaran valors (molt) més curts.
Notes de portabilitat

Aquesta funció no estava disponible a la versió original de la biblioteca Wire i és possible que encara no estigui disponible a totes les plataformes. El codi que ha de ser portàtil entre plataformes i versions pot utilitzar la macro WIRE_HAS_TIMEOUT, que només es defineix quan `Wire.setWireTimeout()`, `Wire.getWireTimeoutFlag()` i `Wire.clearWireTimeout()` estan disponibles.

Quan es va introduir aquesta funció de temps d'espera a la plataforma AVR, inicialment es va mantenir desactivada per defecte per compatibilitat, esperant que s'habiliten més endavant. Això significa que el valor predeterminat del temps d'espera pot variar entre (versions de) plataformes. La configuració de temps d'espera predeterminada està disponible a la macro WIRE_DEFAULT_TIMEOUT i WIRE_DEFAULT_RESET_WITH_TIMEOUT.

Si necessiteu que es desactivi el temps d'espera, es recomana que el desactiveu de manera predeterminada mitjançant `setWireTimeout(0)`, tot i que aquest és el valor predeterminat actualment.

### Vegeu també

LLENGUATGE [Wire](../wire.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
