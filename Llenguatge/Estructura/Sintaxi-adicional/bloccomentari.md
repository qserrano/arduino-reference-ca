---
títol: "* *"
descripció: "bloc de comentaris"
categoria: "Estructura"
subcategoria: "Sintaxi adicional"
---

# /* */

### Descripció

Els comentaris són línies del programa que s'utilitzen per informar-vos a vosaltres mateixos o a altres persones sobre com funciona el programa. El compilador els ignora i no s'exporten al processador, de manera que no ocupen espai a la memòria flash del microcontrolador. L'únic propòsit dels comentaris és ajudar-vos a entendre (o recordar) o informar als altres sobre com funciona el vostre programa.

L'inici d'un comentari de bloc o d'un comentari de diverses línies està marcat amb el símbol /* i el símbol \*/ marca el seu final. Aquest tipus de comentari s'anomena de manera que es pot estendre en més d'una línia; una vegada que el compilador llegeix /* ignora el que segueix fins que troba un \*/.

### Exemple de codi

```
/* Aquest és un comentari vàlid */

/*
  Parpellejar
  Encén un LED durant un segon, després s'apaga durant un segon, repetidament.

  Aquest codi d'exemple és de domini públic.
  (Un altre comentari vàlid)
*/

/*
  if (gwb == 0) { // el comentari d'una sola línia està bé dins d'un comentari de diverses línies
    x = 3;        /* però no un altre comentari de diverses línies; això no és vàlid */
  }
// no oblideu el comentari de "tancament" - s'han d'equilibrar!
*/
```

### Notes i advertències

Quan experimenteu amb codi, "comentar" parts del vostre programa és una manera convenient d'eliminar les línies que poden tenir errors. Això deixa les línies al codi, però les converteix en comentaris, de manera que el compilador simplement les ignora. Això pot ser especialment útil quan s'intenta localitzar un problema, o quan un programa es nega a compilar i l'error del compilador és críptic o no és útil.

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)  
