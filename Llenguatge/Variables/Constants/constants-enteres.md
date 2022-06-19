---
títol: Constants enteres
categoria: [ "Variables" ]
subcategoria: [ "Constants" ]
---

# Constants enteres


## Descripció

Les constants senceres són números que s'utilitzen directament en un esbós, com 123. De manera predeterminada, aquests números es tracten com `int`, però pot canviar això amb els modificadors O i L (consulte a continuació).

Normalment, les constants senceres es tracten com a enters de base 10 (decimals), però es pot usar una notació especial (formatadors) per a ingressar números en altres bases.

| Base | Exemple | Formatador | Comentari
| ---- | ------- | ---------- | ---------
| 10 (decimal) | 123 | Ningun
| 2 (binari) | 0b1111011 | inici "0b" | caràcters 0&1 vàlids
| 8 (octal) | 0173 | inici "0" | caràcters 0-7 vàlids
| 16 (hexadecimal) | 0x7B | inici "0x" 1 caràcters 0-9, A-F, a-f vàlids

### Decimals (base 10)

Aquesta és la matemàtica de sentit comú amb la qual està familiaritzat. Se suposa que les constants sense altres prefixos estan en format decimal.

#### Codi d'exemple:

`n = 101;  // igual que 101 decimal ((1 * 10^2) + (0 * 10^1) + 1)`

### Binari (base 2)

Només són vàlids els caràcters 0 i 1.

#### Exemple de codi:

`n = 0b101; // igual que 5 decimal ((1 * 2^2) + (0 * 2^1) + 1)`

### Octal (base 8)

Només són vàlids els caràcters del 0 al 7. Els valors octals s'indiquen amb el prefix "0" (zero).

#### Exemple de codi:

`n = 0101; // igual que 65 decimal ((1 * 8^2) + (0 * 8^1) + 1)`

### Hexadecimal (base 16)

Els caràcters vàlids són del 0 al 9 i les lletres de la A a la F; A té el valor 10, B és 11, fins a F, que és 15. Els valors hexadecimals s'indiquen amb el prefix "0x". Tingueu en compte que A-F pot ser majúscula (A-F) o minúscula (a-f).

#### Exemple de codi:

`n = 0x101; // igual que 257 decimal ((1 * 16^2) + (0 * 16^1) + 1)`

## Notes i advertències

Formatadors U i L:

De manera predeterminada, una constant entera es tracta com un int amb les limitacions de valors corresponents. Per especificar una constant entera amb un altre tipus de dades, seguiu-la amb:

- una 'u' o 'U' per forçar la constant a un format de dades sense signar. Exemple: 33u
- una 'l' o 'L' per forçar la constant a un format de dades llarg. Exemple: 100000L
- un 'ul' o 'UL' per forçar la constant a una constant llarga sense signar. Exemple: 32767ul

## Vegeu també

LLENGUATGE [Variables](../../Variables.md)  

