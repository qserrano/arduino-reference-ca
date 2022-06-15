---
títol: "isHexadecimalDigit()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isHexadecimalDigit()

### Descripcio

Analitza si un caràcter és un dígit hexadecimal (A-F, 0-9). Retorna true si `thisChar` conté un dígit hexadecimal.

### Sintaxi

`isHexadecimalDigit(thisChar)`

### Paràmetres

`thisChar`: variable. Tipus de dades permesos: char.

### Devolucions

true: si thisChar és un dígit hexadecimal.

### Codi de exemple

```
if (isHexadecimalDigit(myChar)) // tests if myChar is an hexadecimal digit
{
  Serial.println("The character is an hexadecimal digit");
}
else
{
  Serial.println("The character is not an hexadecimal digit");
}
```

### Vegeu també

LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [if (operadors condicionals)](../../Estructura/Control/if.md)  
LLENGUATGE [while (operodars condicionals)](../../Estructura/Control/while.md)  
LLENGUATGE [Serial.read()](../Comunicacio/Serial/read().md)  
LLENGUATGE [Funcions](../../Funcions.md)    
