---
títol: "double"
categories: [ "Variables" ]
subcategories: [ "Tipus de dades" ]
---


# double

## Descripció

Número de coma flotant de doble precisió. En UNO i altres plaques basades en ATMEGA, ocupa 4 bytes. És a dir, la implementació doble és exactament igual que la flotant, sense guanyar en precisió.

En Arduino Due, els dobles tenen una precisió de 8 bytes (64 bits).

## Sintaxi

`doble var = val;`

## Paràmetres

`var`: nom de la variable.  
`val`: el valor a assignar a aqueixa variable.

## Notes i Advertiments

Els usuaris que ampren codi d'altres fonts que inclou variables double poden desitjar examinar el codi per a veure si la precisió implícita és diferent de la que realment s'aconsegueix en Arduinos basats en ATMEGA.

## Veure també

LLENGUATGE [Variables](../../Variables.md)
