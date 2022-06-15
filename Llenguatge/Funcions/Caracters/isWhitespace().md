---
títol: "isWhitespace()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isWhitespace()

### Descripcio

Analitza si un caràcter és un caràcter espai. Retorna cert si l'argument és un espai o una pestanya horitzontal ('\t').

### Sintaxi

`isWhitspace(thisChar)`

### Paràmetres

`thisChar`: variable. Tipus de dades permesos: char.

### Devolucions

true: si thisChar és un caràcter d'espai.

### Codi de exemple

```
if (isWhitespace(myChar)) // tests if myChar is a space character
{
  Serial.println("The character is a space or tab");
}
else {
  Serial.println("The character is not a space or tab");
}
```

### Vegeu també

LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [if (operadors condicionals)](../../Estructura/Control/if.md)  
LLENGUATGE [while (operodars condicionals)](../../Estructura/Control/while.md)  
LLENGUATGE [Serial.read()](../Comunicacio/Serial/read().md)  
LLENGUATGE [Funcions](../../Funcions.md)   
