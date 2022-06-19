---
títol: [scope]
categoria: [ "Variables" ]
subcategoria: [ "Abast de variables" ]
---

# scope

## Descripció

Les variables del llenguatge de programació C++, que utilitza Arduino, tenen una propietat anomenada àmbit (scope). Això contrasta amb les primeres versions d'idiomes com BASIC on cada variable és una variable global.
Una variable global és aquella que pot ser vista per totes les funcions d'un programa. Les variables locals només són visibles per a la funció en què es declaren. A l'entorn Arduino, qualsevol variable declarada fora d'una funció (per exemple, setup(), loop(), etc.), és una variable global.

Quan els programes comencen a ser més grans i complexos, les variables locals són una manera útil d'assegurar-se que només una funció té accés a les seves pròpies variables. Això evita errors de programació quan una funció modifica sense voler variables utilitzades per una altra funció.

De vegades també és útil declarar i inicialitzar una variable dins d'un bucle for. Això crea una variable a la qual només es pot accedir des de l'interior dels claudàtors del bucle.

## Exemple de codi

```
int gPWMval; // qualsevol funció veurà aquesta variable

void setup() {
  //...
}

void loop() {
  int i; // "i" només és "visible" dins del "bucle"
  float f; // "f" només és "visible" dins del "bucle"
  //...

  for (int j = 0; j < 100; j++) {
    // La variable j només es pot accedir dins dels claudàtors del bucle for
  }
}
```

## Vegeu també

LLENGUATGE [Variables](../../Variables.md)  
