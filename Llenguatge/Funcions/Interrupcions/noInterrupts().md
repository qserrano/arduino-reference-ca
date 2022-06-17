---
títol: "noInterrupts()"
descripció: ""
categoria: "Funcions"
subcategoria: "Interrupcions"
---

# noInterrupts()

### Descripció

Desactiva les interrupcions (pots tornar-les a habilitar amb `interrupcions()`). Les interrupcions permeten que es realitzin determinades tasques importants en segon pla i estan habilitades de manera predeterminada. Algunes funcions no funcionaran mentre les interrupcions estiguin desactivades i la comunicació entrant pot ser ignorada. Tanmateix, les interrupcions poden alterar lleugerament el temps del codi i es poden desactivar per a seccions de codi especialment crítiques.

### Sintaxi

`noInterrupsts()`

### Paràmetres

Cap

### Devolucions

Res

### Exemple de codi

El codi mostra com habilitar les interrupcions.
```
void setup() {}

void loop() {
  noInterrupts();
  // critical, time-sensitive code here
  interrupts();
  // other code here
}
```
### Vegeu també

LLENGUATGE [Funcions](../../Funcions.md)  
