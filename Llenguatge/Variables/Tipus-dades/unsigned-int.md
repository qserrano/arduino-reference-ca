---
títol: "unsigned int"
categories: [ "Variables" ]
subcategories: [ "Tipus de dades" ]
---

# unsigned int

## Descripció

A les plaques basades en Uno i altres ATMEGA, els unsigned int (enters sense signe) són els mateixos que els ints ja que emmagatzemen un valor de 2 bytes. En lloc d'emmagatzemar nombres negatius, però, només emmagatzemen valors positius, donant un rang útil de 0 a 65.535 ((2^16) - 1).

El Due emmagatzema un valor de 4 bytes (32 bits), que oscil·la entre 0 i 4.294.967.295 (2^32 - 1).

La diferència entre els ints sense signe i els ints (signats) rau en la manera com s'interpreta el bit més alt, de vegades anomenat bit "signe". En el tipus int d'Arduino (que té el signe), si el bit alt és un "1", el nombre s'interpreta com un nombre negatiu i els altres 15 bits s'interpreten amb (matemàtiques del complement de 2).

## Sintaxi

`unsigned int var = val;`

## Paràmetres

`var`: nom de variable.  
`val`: el valor que assigneu a aquesta variable.

## Exemple de codi

`unsigned int ledPin = 13;`

## Notes i advertències

Quan es fa que les variables sense signar superin la seva capacitat màxima, "recorren" de nou a 0, i també al revés:

```
int x sense sign;
x = 0;
x = x - 1; // x ara conté 65535 - gira en direcció neg
x = x + 1; // x ara conté 0 - es passa
```

Les matemàtiques amb variables sense signar poden produir resultats inesperats, fins i tot si la vostra variable sense signar mai es revertí.

La MCU aplica les regles següents:

El càlcul es fa en l'àmbit de la variable de destinació. Per exemple. si la variable de destinació està signada, farà matemàtiques amb signes, encara que ambdues variables d'entrada no estiguin signades.

Tanmateix, amb un càlcul que requereix un resultat intermedi, el codi no especifica l'abast del resultat intermedi. En aquest cas, l'MCU farà matemàtiques sense signe per al resultat intermedi, perquè ambdues entrades no tenen signe!

```
int sense signe x = 5;
sense signe int y = 10;
int resultat;

resultat = x - y; // 5 - 10 = -5, com s'esperava
resultat = (x - y) / 2; // 5 - 10 en matemàtiques sense signar és 65530! 65530/2 = 32765

// solució: utilitzeu variables signades o feu el càlcul pas a pas.
resultat = x - y; // 5 - 10 = -5, com s'esperava
resultat = resultat / 2; // -5/2 = -2 (només matemàtiques enteres, s'eliminen els decimals)
```

Per què utilitzar variables sense signar?
- Es desitja el comportament d'enrotllament, p.e. comptadors
- La variable signada és una mica massa petita, però voleu evitar la pèrdua de memòria i velocitat de long/float.

## Vegeu també

LLENGUATGE [Constants enteres](../Constants/constants-enteres.md)  
LLENGUATGE [Variables](../../Variables.md)
