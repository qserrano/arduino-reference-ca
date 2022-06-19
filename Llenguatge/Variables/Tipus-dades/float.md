---
títol: "float"
categories: [ "Variables" ]
subcategories: [ "Tipus de dades" ]
---

# float

## Descripció

Tipus de dades per a números de punt flotant, un número que té un punt decimal. Els números de coma flotant sovint s'usen per a aproximar valors analògics i continus perquè tenen una resolució major que els nombres enters. Els números de punt flotant poden ser tan grans com 3,4028235E+38 i tan baixos com -3,4028235E+38.

S'emmagatzemen com 32 bits (4 bytes) d'informació.

## Sintaxi

`flotant var = valor;`

## Paràmetres

`var`: nom de la variable.  
`val`: el valor que assignes a aqueixa variable.

##Codi d'exemple

```
float myfloat;
float sensorCalbrate = 1.117;

int x;
int y;
float z;

x = 1;
y = x / 2;          // y now contains 0, ints can't hold fractions
z = (float)x / 2.0; // z now contains .5 (you have to use 2.0, not 2)
```

## Notes i Advertiments

Si fa operacions matemàtiques amb flotants, ha d'agregar un punt decimal; en cas contrari, es tractarà com un int. Veja la pàgina de [constants de punt flotant](../Constants/coma-flotant.md) per a més detalls.

El tipus de dades flotant té només 6-7 dígits decimals de precisió. Això significa el nombre total de dígits, no el número a la dreta del punt decimal. A diferència d'altres plataformes, on pot obtindre més precisió utilitzant un double (per exemple, fins a 15 dígits), en Arduino, el doble té la mateixa grandària que el float.

Els números de punt flotant no són exactes i poden produir resultats estranys quan es comparen. Per exemple, 6.0/3.0 pot no ser igual a 2.0. En el seu lloc, ha de verificar que el valor absolut de la diferència entre els números siga menor que un número xicotet.

La conversió de punt flotant a nombres enters resulta en truncament:

```
float x = 2.9; // A float type variable
int y = x;  // 2
```

Si, en canvi, desitja arredonir durant el procés de conversió, ha d'agregar 0.5:

```
float x = 2.9;
int y = x + 0.5;  // 3
```

o usa la funció round():

```
float x = 2.9;
int y = round(x);  // 3
```

Les matemàtiques de punt flotant també són molt més lentes que les matemàtiques de nombres enters en la realització de càlculs, per la qual cosa han d'evitar-se si, per exemple, un bucle ha d'executar-se a la màxima velocitat per a una funció de temps crítica. Els programadors sovint fan tot el possible per a convertir els càlculs de coma flotant en matemàtiques senceres per a augmentar la velocitat.

## Veure també

LLENGUATGE [Variables](../../Variables.md)
