---
títol: "isAlpha()"
descripció: ""
categoria: "Funcions"
subcategoria: "Caracters"
---

# isAlpha()

### Descripció

Analitza si un char és alfa (és una lletra). Retorna vertader si thisChar conté una lletra.

### Sintaxi

`isAlpha(thisChar)`

### Paràmetres

`thisChar`: variable. Tipus de dades permeses: char.

### Devolucions

True: si thisChar és alfa.

### Codi d'exemple

```
if (isAlpha(myChar)) {  // tests if myChar is a letter
  Serial.println("The character is a letter");
}
else {
  Serial.println("The character is not a letter");
}
```

### Veure també

LLENGUATGE [char](../../Variables/Tipus-dades/char.md)  
LLENGUATGE [if](../../Estructura/Operadors-condicionals/if.md) (operadors condicionals)  
LLENGUATGE [while](../../Estructura/Operadors-condicionals/while.md) (operadors condicionals)  
LLENGUATGE [Serial.read()](../Comunicació/Serial/Serial.read().md)  
LLENGUATGE [Funcions](../../Funcions.md)  
