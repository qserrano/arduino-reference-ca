---
títol: "isAscii()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isAscii()

### Descripció

Analitza si un char és Ascii. Retorna vertader si thisChar conté un caràcter ASCII.

### Sintaxi

`isAscii(thisChar)`

### Paràmetres

`thisChar`: variable. Tipus de dades permeses: char.

### Devolucions

True: si thisChar és Ascii.

### Codi d'exemple

```
if (isAscii(myChar)) {  // tests if myChar is an Ascii character
  Serial.println("The character is Ascii");
}
else {
  Serial.println("The character is not Ascii");
}
```

### Vegeu també

LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [if (operadors condicionals)](../../Estructura/Control/if.md)  
LLENGUATGE [while (operodars condicionals)](../../Estructura/Control/while.md)  
LLENGUATGE [Serial.read()](../Comunicacio/Serial/read().md)  
LLENGUATGE [Funcions](../../Funcions.md)    
