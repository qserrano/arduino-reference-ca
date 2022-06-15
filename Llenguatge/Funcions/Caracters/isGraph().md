---
títol: "isGraph()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isGraph()

### Descripció

Analitza si un caràcter és pot imprimir amb algun contingut (l'espai és imprimible però no te contingut). Retorna true si thisChar és imprimible.

### Syntax

`isGraph(thisChar)`

### Parameters

`thisChar`: variable. Tipus de dades permesos: char.

### Returns

true: si thisChar és imprimible.

### Example Code

```
if (isGraph(myChar))
{  // tests if myChar is a printable character but not a blank space.
  Serial.println("The character is printable");
}
else
{
  Serial.println("The character is not printable");
}
```

### Vegeu també

LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [if (operadors condicionals)](../../Estructura/Control/if.md)  
LLENGUATGE [while (operodars condicionals)](../../Estructura/Control/while.md)  
LLENGUATGE [Serial.read()](../Comunicacio/Serial/read().md)  
LLENGUATGE [Funcions](../../Funcions.md)    
