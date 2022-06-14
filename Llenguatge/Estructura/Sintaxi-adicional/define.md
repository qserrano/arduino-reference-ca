---
títol: "#define"
descripció: ""
categoria: "Estructura"
subcategoria: "Sintaxi adicional"
---

# #define

### Descripció

\#define és un component útil de C++ que permet al programador donar un nom a un valor constant abans de compilar el programa. Les constants definides en arduino no ocupen cap espai de memòria de programa en el xip. El compilador reemplaçarà les referències a aquestes constants amb el valor definit en el moment de la compilació.

Tanmateix, això pot tindre alguns efectes secundaris no desitjats, si per exemple, un nom de constant que ha sigut definit s'inclou en algun altre nom de constant o variable. En aqueix cas, el text seria reemplaçat pel número (o text) definit.

En general, es prefereix la paraula clau const per a definir constants i ha d'usar-se en lloc de #define.

### Sintaxi

`#define constantName value`

### Paràmetres

`constantName`: el nom de la macro a definir.  
`value`: el valor a assignar a la macro.

### Codi d'exemple

```
#define ledPin 3
// El compilador reemplaçarà qualsevol esment de ledPin amb el valor 3 en el moment de la compilació.
```

### Notes i Advertiments

No hi ha punt i coma després de la instrucció #define. Si inclou un, el compilador llançarà errors críptics més a baix en la pàgina.

```
#define ledPin 3; // aço es un error
```

De manera similar, incloure un signe igual després de la declaració #define també generarà un error de compilació críptic més a baix en la pàgina.

```
#define ledPin  = 3 // aço tambe es un error
```

### Vegeu també

LLENGUATGE [constant](../../Variables/Abast-variable/const.md)  
LLENGUATGE [Constants](../../Variables/Constants/constants.md)  
LLENGUATGE [Estructura](../../Estructura.md)  
