---
títol: "isDigit()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isDigit()

### Descripció

Analitza si un char és un dígit (és a dir, un número). Retorna vertader si thisChar és un número.

### Sintaxi

`isDigit(thisChar)`

### Paràmetres

`thisChar`: variable. Tipus de dades permeses: char.

### Devolucions

True: si thisChar és un número.

### Codi d'exemple

```
if (isDigit(myChar)) {  // tests if myChar is a digit
  Serial.println("The character is a number");
}
else {
  Serial.println("The character is not a number");
}
```

### Vegeu també

LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [if (operadors condicionals)](../../Estructura/Control/if.md)  
LLENGUATGE [while (operodars condicionals)](../../Estructura/Control/while.md)  
LLENGUATGE [Serial.read()](../Comunicacio/Serial/read().md)  
LLENGUATGE [Funcions](../../Funcions.md)    
