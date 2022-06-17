---
títol: "pulseIn()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Avançades"
---

# pulseIn()

### Descripció

Llig un pols (ja siga ALT o BAIX) en un pin. Per exemple, si el valor és ALT, `pulseIn()` espera al fet que el pin passe de BAIX a ALT, comença a cronometrar, després espera al fet que el pin passe a BAIX i deté el cronometratge. Retorna la longitud del pols en microsegons o es dona per vençut i retorna 0 si no es
va rebre cap pols complet dins del temps d'espera.

El temps d'aquesta funció ha sigut determinat empíricament i probablement mostrarà errors en polsos més llargs. Funciona amb polsos de 10 microsegons a 3 minuts de duració.

**Nota**: si s'usa el temps d'espera opcional, el codi s'executarà més ràpid.

### Sintaxi

`pulseIn(pin, value)`  
`pulseIn(pin, value, timeout)`  

### Paràmetres

`pin`: el número del pin Arduino en el qual desitja llegir el pols. Tipus de dades permeses: int.  
`value`: tipus de pols a llegir: [HIGH o LOW](../../Variables/Constants/high-low.md). Tipus de dades permeses: int.  
`timeout` (opcional): el nombre de microsegons a esperar perquè comence el pols; el valor predeterminat és un segon. Tipus de dades permeses: unsigned long.

### Devolucions

La duració del pols (en microsegons) o 0 si no es va iniciar cap pols abans del temps d'espera. Tipus de dades: unsigned long

### Codi d'exemple

L'exemple imprimeix el temps de duració d'un pols en el pin 7.

```
int pin = 7;
unsigned long duration;

void setup()
{
  Serial.begin(9600);
  pinMode(pin, INPUT);
}

void loop()
{
  duration = pulseIn(pin, HIGH);
  Serial.println(duration);
}
```

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
