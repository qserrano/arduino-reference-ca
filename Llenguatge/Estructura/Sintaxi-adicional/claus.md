---
títol: "{ }"
descripció: "Final de declaracio"
categoria: "Estructura"
subcategoria: "Sintaxi adicional"
---

# {}

### Descripció

Les claus (també conegudes com a "tirants" o "claudàtors") són una part important del llenguatge de programació C++. S'utilitzen en diverses construccions diferents, que es descriuen a continuació, i això de vegades pot ser confús per als principiants.

Una clau d'obertura { sempre ha d'anar seguida d'una clau de tancament }. Aquesta és una condició que sovint s'anomena equilibri dels tirants. L'IDE d'Arduino (entorn de desenvolupament integrat) inclou una característica convenient per comprovar l'equilibri de les claus. Només cal que seleccioneu una clau, o fins i tot feu clic al punt d'inserció immediatament després d'una clau, i el seu acompanyant lògic es ressaltarà.

Els programadors principiants i els programadors que arriben a C++ des del llenguatge BASIC sovint troben l'ús de claus confús o descoratjador. Després de tot, les mateixes claus substitueixen la instrucció RETURN en una subrutina (funció), la sentència ENDIF en un condicional i la sentència NEXT en un bucle FOR.

Les claus desequilibrades sovint poden provocar errors del compilador críptics i impenetrables que de vegades poden ser difícils de localitzar en un programa gran. A causa dels seus usos variats, les claus també són increïblement importants per a la sintaxi d'un programa i moure una clau o dues línies sovint afectarà dràsticament el significat d'un programa.

### Exemple de codi

Els principals usos de les claus es mostren als exemples següents.

**Funcions**

```
void myfunction (argument del tipus de dades) {
  // qualsevol declaració(s)
}
```

**Bucles**

```
while (expressió booleana) {
  // qualsevol declaració(s)
}

do {
  // qualsevol declaració(s)
} while (expressió booleana);

for (inicialització; condició de terminació; expr incrementant) {
  // qualsevol declaració(s)
}
```

**Declaracions condicionals**

```
if (expressió booleana) {
  // qualsevol declaració(s)
}

else if (expressió booleana) {
  // qualsevol declaració(s)
}

else {
  // qualsevol declaració(s)
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)  
