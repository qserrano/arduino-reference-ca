---
títol: "puseInLong()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Avançades"
---

# pulseInLong()

### Descripció

`pulseInLong()` és una alternativa a `pulseIn()` que és millor en el maneig de polsos llargs i escenaris afectats per interrupcions.

Llig un pols (ja siga HIGH o LOW) en un pin. Per exemple, si el valor és HIGH, `pulseInLong()` espera al fet que el pin passe de LOW a HIGH, comença a cronometrar, després espera al fet que el pin passe a LOW i deté el cronometratge. Retorna la longitud del pols en microsegons o es dona per vençut i retorna 0 si no es va rebre cap pols complet dins del temps d'espera.

El temps d'aquesta funció ha sigut determinat empíricament i probablement mostrarà errors en polsos més curts. Funciona amb polsos de 10 microsegons a 3 minuts de duració. Aquesta rutina es pot usar només si les interrupcions estan activades. A més, la resolució més alta s'obté amb intervals grans.

### Sintaxi

`pulseInLong(pin, value)`  
`pulseInLong(pin, value, timeout)`  

### Paràmetres

`pin`: el número del pin Arduino en el qual desitja llegir el pols. Tipus de dades permeses: int.  
`value`: tipus de pols a llegir: ALT o BAIX. Tipus de dades permeses: int.  
`timeout` (opcional): el nombre de microsegons a esperar perquè comence el pols; el valor predeterminat és un segon. Tipus de dades permeses: llarg sense signar.

### Devolucions

La duració del pols (en microsegons) o 0 si no es va iniciar cap pols abans del temps d'espera. Tipus de dades: llarg sense signar.

### Codi d'exemple

L'exemple imprimeix el temps de duració d'un pols en el pin 7.

```
int pin = 7;
unsigned long duration;

void setup() {
  Serial.begin(9600);
  pinMode(pin, INPUT);
}

void loop() {
  duration = pulseInLong(pin, HIGH);
  Serial.println(duration);
}
```

### Notes i advertències

Aquesta funció es basa en `micros()` per tant no es pot utilitzar en el context `noInterrupts()`.

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
