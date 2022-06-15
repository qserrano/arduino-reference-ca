---
títol: "isPrintable()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isPrintable()

### Descripcio

Analitza si un caràcter és imprimible (és a dir, qualsevol caràcter que produeixi una sortida, fins i tot un espai en blanc). Retorna true si thisChar és imprimible.

### Sintaxi

`isPrintable(thisChar)`

### Paràmetres

`thisChar`: variable. Tipus de dades permesos: char.

### Devolucions

true: si thisChar és imprimible.

### Codi de exemple

```
if (isPrintable(myChar)) // tests if myChar is printable char
{  
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
