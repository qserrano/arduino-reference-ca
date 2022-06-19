---
títol: [sizeof()]
categoria: [ "Variables" ]
subcategoria: [ "Utilitats" ]
---

# sizeof()

## Descripció

L'operador `sizeof` retorna el nombre de bytes en un tipus de variable o el nombre de bytes ocupats per una matriu.

## Sintaxi

`sizeof(variable)`

## Paràmetres

`variable`: la cosa per obtenir la mida. Tipus de dades permesos: qualsevol tipus de variable o matriu (per exemple, int, float, byte).

## Devolucions

El nombre de bytes d'una variable o bytes ocupats en una matriu. Tipus de dades: size_t.

## Exemple de codi

L'operador sizeof és útil per tractar amb matrius (com cadenes) on és convenient poder canviar la mida de la matriu sense trencar altres parts del programa.

Aquest programa imprimeix una cadena de text un caràcter a la vegada. Prova de canviar la frase del text.

```
char myStr[] = "això és una prova";

void setup() {
  Serial.begin(9600);
}

void loop() {
  for (byte i = 0; i < sizeof(myStr) - 1; i++) {
    Serial.print(i, DEC);
    Serial.print(" = ");
    Serial.write(myStr[i]);
    Serial.println();
  }
  delay (5000); // alentir el programa
}
```

## Notes i advertències

Tingueu en compte que `sizeof` retorna el nombre total de bytes. Per tant, per a matrius de tipus variables més grans, com ara ints, el bucle for seria semblant a això.

```
int myValues[] = {123, 456, 789};

// aquest bucle for funciona correctament amb una matriu de qualsevol tipus o mida
for (byte i = 0; i < (sizeof(myValues) / size0f(myValues[0])); i++) {
  // fer alguna cosa amb myValues[i]
}
```

Tingueu en compte que una cadena formatada correctament acaba amb el símbol NULL, que té el valor ASCII 0.

## Vegeu també

LLENGUATGE [Variables](../../Variables.md)
