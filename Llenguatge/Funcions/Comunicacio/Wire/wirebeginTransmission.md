---
títol: "Wire.beginTransmission()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Wire"
---

# beginTransmission()

### Descripció

Aquesta funció inicia una transmissió al dispositiu perifèric I2C amb l'adreça proporcionada. Posteriorment, pose en cua bytes per a la transmissió amb la funció `write()` i els transmet cridant a endTransmission().

### Sintaxi

`Wire.beginTransmission (adreça)`  

### Paràmetres

`Adreça`: l'adreça de 7 bits del dispositiu per transmetre.  

### Devolucions

Cap.

### Vegeu també

LLENGUATGE [Wire](../wire.md)  
LLENGUATGE [Funcions](../../../Funcions.md)

