---
títol: else
descripció: ""
categoria: "Estructura"
subcategoria: "Control"
---

# else

### Descripció

La `if…else` permet un major control sobre el flux de codi que la instrucció `if` bàsica, en permetre que s'agrupen múltiples proves. S'executarà una clàusula `else` (si és que existeix) si la condició en la declaració `if` dona com a resultat fals. La `else` pot continuar amb una altra prova `if`, de manera que es poden executar diverses proves mútuament excloents al mateix temps.

Cada prova passarà a la següent fins que es trobe una prova vertadera. Quan es troba una prova vertadera, s'executa el seu bloc de codi associat i el programa salta a la línia que segueix a tota la construcció `if`/`else`. Si cap prova resulta ser certa, s'executa el bloc `else` predeterminat, si hi ha un present, i estableix el comportament predeterminat.

Tinga en compte que un bloc `else if` pot usar-se amb o sense un bloc `else` de terminació i viceversa. Es permet un número il·limitat de branques.

### Sintaxi

```
if (condition1) {
  // do Thing A
}
else if (condition2) {
  // do Thing B
}
else {
  // do Thing C
}
```

### Codi d'exemple

A continuació es mostra un extracte d'un codi per al sistema de sensor de temperatura

```
if (temperature >= 70) {
  // Perill! Apague el sistema.
}
else if (temperature >= 60) { // 60 <= temperature < 70
   // Advertiment! Es requereix atenció de l'usuari.
}
else { // temperature < 60
  // Fora de perill! Continuar amb les tasques habituals.
}
```

### Vegeu també

LLENGUATGE [Estructura](../../Estructura.md)
