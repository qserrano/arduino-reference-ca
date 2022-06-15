---
títol: "isAlphaNumeric()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isAlphaNumeric()

### Descripció

Analitza si un char és alfanumèric (és a dir, una lletra o un número). Retorna vertader si thisChar conté un número o una lletra.

### Sintaxi

`isAlphaNumeric(thisChar)`

### Paràmetres

`thisChar`: variable. Tipus de dades permeses: char.

### Devolucions

True: si thisChar és alfanumèric.

### Codi d'exemple

```
if (isAlphaNumeric(myChar)) { // tests if myChar isa letter or a number
  Serial.println("The character is alphanumeric");
}
else {
  Serial.println("The character is not alphanumeric");
}
```

### Vegeu també

LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [if](../../Estructura/Operadors-condicionals/if.md) (operadors condicionals)  
LLENGUATGE [while](../../Estructura/Operadors-condiconals/while.md) (operadors condicionas)  
LLENGUATGE [read](../Funcions/Serial/Serial.read().md)()  
LLENGUATGE [Funcions](../../Funcions.md)    
