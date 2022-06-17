---
títol: "map()"
descripció: ""
categoria: "Funcions"
subcategoria: "Matematiques"
---

# map()

### Descripció

Torna a assignar un número d'un rang a un altre. És a dir, un valor de fromLow s'assignaria a toLow, un valor de fromHigh a toHigh, valors intermedis a valors intermedis, etc.

No restringeix els valors dins del rang, perquè els valors fora del rang a vegades són intencionats i útils. La funció `constrain()` pot usar-se abans o després d'aquesta funció, si es desitgen límits als rangs.

Tinga en compte que els "límits inferiors" de qualsevol dels rangs poden ser més grans o més xicotets que els "límits superiors", per la qual cosa la funció `map()` es pot usar per a invertir un rang de números, per exemple

`y = map(x, 1, 50, 50, 1);`

La funció també maneja bé els números negatius, per la qual cosa aquest exemple

`y = map(x, 1, 50, 50, -100);`

també és vàlid i funciona bé.

La funció map() usa matemàtiques senceres, per la qual cosa no generarà fraccions, quan les matemàtiques podrien indicar que hauria de fer-ho. Les restes fraccionàries es trunquen i no s'arredoneixen ni es fan una mitjana.

### Sintaxi

`map(value, fromLow, fromHigh, toLow, toHigh)`

### Paràmetres

`value`: el número a mapear.  
`fromLow`: el límit inferior del rang actual del valor.  
`fromHigh`: el límit superior del rang actual del valor.  
`toLow`: el límit inferior del rang objectiu del valor.  
`toHigh`: el límit superior del rang objectiu del valor.  

### Devolucions

El valor mapetjat.


### Codi d'exemple

```
/* Assigna un valor analogic (0 - 1023) a un de 8 bits (0 - 255) */

void setup() {}

void loop()
{
  int val = analogRead(0);
  val = map(val, 0, 1023, 0, 255);
  analogWrite(9, val);
}
```

### Apèndix

Per als inclinats a les matemàtiques, ací està la funció completa

```
long map(long x, long in_min, long in_max, long out_min, long out_max) {
  return (x - in_min) * (out_max - out_min) / (in_max - in_min) + out_min;
}
```

### Notes i advertiments

Com es va esmentar anteriorment, la funció map() usa matemàtiques senceres. Llavors, les fraccions poden suprimir-se a causa d'això. Per exemple, fraccions com 3/2, 4/3, 5/4 es retornaran totes com 1 des de la funció map(), malgrat els seus diferents valors reals. Llavors, si el seu projecte requereix càlculs precisos (per exemple, voltatge amb precisió de 3 decimals), considere evitar map() i
implementar els càlculs manualment en el seu codi vosté mateix.

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
