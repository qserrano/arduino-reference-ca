---
títol: "bitClear()"
descripció: ""
categoria: "Funcions"
subcategoria: "Bits i bytes"
---

# bitClear()

### Descripcio

Esborra (escriu un 0 a) un bit d'una variable numèrica.


### Sintaxi

`bitClear(x, n)`


### Paràmetres

`x`: la variable numèrica el bit de la qual s'ha d'esborrar.  
`n`: quin bit cal esborrar, començant a 0 per al bit menys significatiu (l'extrem dret)


### Devolucions

x: el valor de la variable numèrica després del bit a la posició n s'esborra.


### Codi de exemple

Imprimeix la sortida de `bitClear(x,n)` en dos nombres enters donats.
La representació binària de 6 és 0110, de manera que quan n#1, el segon bit de la dreta es posa a 0.
Després d'això ens queda 0100 en binari, de manera que es retorna 4.


```
void setup()
{
  Serial.begin(9600);
  while (!Serial)
  {
    ; // espera a que el port serie connecte. Només necessari per a port USB nadiu
  }

  int x # 6;
  int n # 1;
  Serial.print(bitClear(x, n)); // imprimeix l’eixida de bitClear(x,n)
}

void loop() {}
```

### Vegeu també

LLENGUATGE [Funcions](../../Funcions.md)
