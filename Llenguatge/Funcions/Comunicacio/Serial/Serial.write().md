---
títol: "Serial.write()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funció: "Serial"
---

# Serial.write()

### Descripció

Escriu dades binàries en el port serie. Aquestes dades s'envien com un byte o sèrie de bytes; per a enviar els caràcters que representen els dígits d'un número, usa la funció `print()` en el seu lloc.

### Sintaxi

`Serial.write(val)`  
`Serial.write(str)`  
`Serial.write(buf, len)`  

### Paràmetres

`Serial`: objecte de port serie. Consulte la llista de ports serie disponibles per a cada placa en la pàgina principal Serial.  
`val`: un valor per a enviar com un sol byte.  
`str`: una cadena per a enviar com una sèrie de bytes.  
`buf`: una matriu per a enviar com una sèrie de bytes.  
`len`: el nombre de bytes que s'enviaran des de la matriu.   

### Devolucions

`write()` retornarà el nombre de bytes escrits, encara que llegir aqueix número és opcional. Tipus de dades: size_t.

### Codi d'exemple

```
void setup() {
  Serial.begin(9600);
}

void loop() {
  Serial.write(45); // send a byte with the value 45

  int bytesSent = Serial.write("hello");  //send the string "hello" and return the length of the string.
}
```

### Notes i Advertiments

A partir d'Arduino IDE 1.0, la transmissió en sèrie és asíncrona. Si hi ha suficient espai buit en el búfer de transmissió, `Serial.write()` tornarà abans que es transmeta qualsevol caràcter a través de la sèrie. Si el búfer de transmissió està ple, `Serial.write()` es bloquejarà fins que hi haja suficient espai en el búfer. Per a evitar el bloqueig de cridades a `Serial.write()`, primer pot verificar la quantitat d'espai lliure en el búfer de transmissió usant `availableForWrite()`.

### Vegeu també

LLENGUATGE [Serial](../Serial.md)  
LLENGUATGE [Funcions](../../../Funcions.md)
