---
títol: "interrupts()"
descripció: ""
categoria: "Funcions"
subcategoria: "Interrupcions"
---

# interrupts()

### Descripció

Torna a activar les interrupcions (després d'haver estat desactivades per `noInterrupts()`. Les interrupcions permeten que es realitzin determinades tasques importants en segon pla i s'activen de manera predeterminada. Algunes funcions no funcionaran mentre les interrupcions estiguin desactivades i la comunicació entrant pot ser ignorada. `interrupts()` pot alterar lleugerament el temps del codi, tanmateix, es pot desactivar per a seccions de codi especialment crítiques.

### Sintaxi

`interrupts()`

### Paràmetres

Cap

### Devolucions

Res

### Exemple de codi

El codi activa les interrupcions.

```
void setup() {}

void loop()
{
  noInterrupts();
  // critical, time-sensitive code here
  interrupts();
  // other code here
}
```

### Vegeu també

LLENGUATGE [ attachInterrupts() ](../Interrupcions-externes/attachInterrupt.md)  
LLENGUATGE [ detachInterrupts() ](../Interrupcions-externes/dettachInterrupt.md)  
LLENGUATGE [Funcions](../../Funcions.md)  
