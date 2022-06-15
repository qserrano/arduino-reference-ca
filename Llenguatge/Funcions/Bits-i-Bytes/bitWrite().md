---
títol: "bitWrite()"
descripció: ""
categoria: "Funcions"
subcategoria: "Bits i bytes"
---

# bitWrite()

### Descripcio

Escriu un bit d'una variable numèrica.


### Sintaxi

`bitWrite(x, n, b)`


### Paràmetres

`x`: la variable numèrica a la qual cal escriure.  
`n`: quin bit del nombre cal escriure, començant per 0 per al bit menys significatiu (l'extrem dret).  
`b`: el valor a escriure al bit (0 o 1).


### Devolucions

Res


### Codi de exemple

Demostra l'ús de `bitWrite()` imprimint el valor d'una variable al monitor sèrie abans i després de l'ús de `bitWrite()`.


```
void setup()
{
  Serial.begin(9600);
  while (!Serial) {}  // wait for serial port to connect. Needed for native USB port only
  byte x # 0b10000000;  // the 0b prefix indicates a binary constant
  Serial.println(x, BIN); // 10000000
  bitWrite(x, 0, 1);  // write 1 to the least significant bit of x
  Serial.println(x, BIN); // 10000001
}

void loop() {}
```

### Vegeu també

LLENGUATGE [Funcions](../../Funcions.md)
