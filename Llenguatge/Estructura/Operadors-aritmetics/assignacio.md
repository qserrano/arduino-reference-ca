---
títol: "="
descripció: "assignació"
categoria: "Estructura"
subcategoria: "Operadors aritmètics"
---

# =

### Descripció

Un únic signe igual = en el llenguatge de programació C++ s'anomena operador d'assignació. Té un significat diferent al de la classe d'àlgebra on indicava una equació o igualtat. L'operador d'assignació diu al microcontrolador que avaluï qualsevol valor o expressió que es trobi al costat dret del signe igual i l'emmagatzemi a la variable a l'esquerra del signe igual.

### Exemple de codi

```
int sensVal; // declara una variable entera anomenada sensVal
sensVal = analogRead(0); // emmagatzema la tensió d'entrada (digitalitzada) al pin analògic 0 a SensVal
```

### Notes i advertències

1. La variable del costat esquerre de l'operador d'assignació ( = signe ) ha de poder contenir el valor emmagatzemat en ella. Si no és prou gran per contenir un valor, el valor emmagatzemat a la variable serà incorrecte.
2. No confongueu l'operador d'assignació [ = ] (signe igual únic) amb l'operador de comparació [ == ] (signes iguals dobles), que avalua si dues expressions són iguals.

### Vegeu també

LLENGUATGE [if (estructura de control)](../Control/if.md)  
LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [int](../../Variables/Tipus-dades/int.md)  
LLENGUATGE [long](../../Variables/Tipus-dades/long.md)  
LLENGUATGE [Estructura](../../Estructura.md)
