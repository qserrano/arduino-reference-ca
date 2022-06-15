---
títol: "isSpace()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isSpace()

### Descripcio

Analitza si un caràcter és un caràcter d'espai en blanc. Retorna true si l'argument és un espai, un feed de formulari ('\f'), una nova línia ('\n'), un retorn de carro ('\r'), una pestanya horitzontal ('\t') o una pestanya vertical ('\ v').

### Sintaxi

`isSpace(thisChar)`

### Paràmetres

`thisChar`: variable. Tipus de dades permesos: char.

### Devolucions

true: si thisChar és un caràcter d'espai en blanc.

### Codi de exemple

```
if (isSpace(myChar)) // tests if myChar is a white-space character
{  
  Serial.println("The character is white-space");
}
else
{
  Serial.println("The character is not white-space");
}
```

### Vegeu també

LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [if (operadors condicionals)](../../Estructura/Control/if.md)  
LLENGUATGE [while (operodars condicionals)](../../Estructura/Control/while.md)  
LLENGUATGE [Serial.read()](../Comunicacio/Serial/read().md)  
LLENGUATGE [Funcions](../../Funcions.md)   
