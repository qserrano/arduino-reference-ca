---
títol: "isControl()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isControl()

### Descripció

Analitza si un char és un caràcter de control. Retorna vertader si thisChar és un caràcter de control.

### Sintaxi

`isControl(thisChar)`

### Paràmetres

`thisChar`: variable. Tipus de dades permeses: char.

### Devolucions

True: si thisChar és un caràcter de control.

### Codi d'exemple

```
if (isControl(myChar)) {  // tests if myChar is a control character
  Serial.println("The character is a control character");
}
else {
  Serial.println("The character is not a control character");
}
```

### Vegeu també

LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [if (operadors condicionals)](../../Estructura/Control/if.md)  
LLENGUATGE [while (operodars condicionals)](../../Estructura/Control/while.md)  
LLENGUATGE [Serial.read()](../Comunicacio/Serial/read().md)  
LLENGUATGE [Funcions](../../Funcions.md)    
