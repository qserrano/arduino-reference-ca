---
títol: if
descripció: ""
categoria: "Estructura"
subcategoria: "Control"
---

# if

### Descripció

La declaració `if` verifica una condició i executa la següent declaració o conjunt de declaracions si la condició és 'vertadera'.

### Sintaxi

```
if (condition) {
  //statement(s)
}
```

### Paràmetres

`condition`: una expressió booleana (és a dir, pot ser vertadera o falsa).

### Codi d'exemple

Els claudàtors poden ometre's després d'una declaració `if`. Si es fa això, la següent línia (definida pel punt i coma) es converteix en l'única declaració condicional.

```
if (x > 120) digitalWrite(LEDpin, HIGH);

if (x > 120)
digitalWrite(LEDpin, HIGH);

if (x > 120) {digitalWrite(LEDpin, HIGH);}

if (x > 120) {
  digitalWrite(LEDpin1, HIGH);
  digitalWrite(LEDpin2, HIGH);
}
// totes son correctes
```

### Notes i Advertiments

Les declaracions que s'avaluen dins dels parèntesis requereixen l'ús d'un o més operadors que es mostren a continuació.

Operadors de comparació:
*  x == i (x és igual a i)
*  x != i (x no és igual a i)
*  x < i (x és menor que i)
*  x > i (x és major que i)
*  x <= i (x és menor o igual que i)
*  x >= i (x és major o igual que i)

Vaja amb compte amb l'ús accidental del signe igual únic (per exemple, si (x = 10)). L'únic signe igual és l'operador d'assignació i estableix x en 10 (posa el valor 10 en la variable x). En el seu lloc, utilitze el signe igual doble (per exemple, si (x == 10)), que és l'operador de comparació i comprova si x és igual a 10 o no. L'última afirmació només és vertadera si x és igual a 10, però la primera afirmació sempre serà vertadera.

Això es deu al fet que C++ avalua la declaració if (x=10) de la següent manera: 10 s'assigna a x (recorde que l'únic signe igual és el (operador d'assignació)), per la qual cosa x ara conté 10. Després, el condicional 'if' avalua 10 , que sempre s'avalua com a VERTADER, ja que qualsevol número diferent de zero s'avalua com a VERTADER. En conseqüència, si (x = 10) sempre s'avaluarà com a VERTADER, que no és el resultat desitjat quan s'usa una declaració 'si'. A més, la variable x s'establirà en 10, que tampoc és una acció desitjada.

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
