---
títol: "isPunct()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isPunct()

### Descripcio

Analitzeu si un caràcter és signe de puntuació (és a dir, una coma, un punt i coma, un signe d'exclamació, etc.).

Retorna true si thisChar és una puntuació.

### Sintaxi

`isPunct(thisChar)`

### Paràmetres

`thisChar`: variable. Tipus de dades permesos: char.

### Devolucions

true: si thisChar és una puntuació.

### Codi de exemple

```
if (isPunct(myChar)) // tests if myChar is a punctuation character
{  
  Serial.println("The character is a punctuation");
}
else
{
  Serial.println("The character is not a punctuation");
}
```

### Vegeu també

LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [if (operadors condicionals)](../../Estructura/Control/if.md)  
LLENGUATGE [while (operodars condicionals)](../../Estructura/Control/while.md)  
LLENGUATGE [Serial.read()](../Comunicacio/Serial/read().md)  
LLENGUATGE [Funcions](../Funcions.md)   
