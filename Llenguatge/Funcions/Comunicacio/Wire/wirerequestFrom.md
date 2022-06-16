---
títol: "Wire.requestFrom()"
descripció: ""
categoria: "Funcions"
subcategoria: "Comunicacio"
funcio: "Wire"
---

# requestFrom()

### Descripció

El dispositiu controlador utilitza aquesta funció per a sol·licitar bytes d'un dispositiu perifèric. Després, els bytes es poden recuperar amb les funcions `available()` i `read()`. A partir d'Arduino 1.0.1, `requestFrom()` accepta un argument booleà que canvia el seu comportament per a compatibilitat amb uns certs dispositius I2C. Si és vertader, `requestFrom()` envia un missatge de detenció després de la sol·licitud, alliberant el bus I2C. Si és fals, `requestFrom()` envia un missatge de reinici després de la sol·licitud. El bus no s'alliberarà, la qual cosa evita que un altre dispositiu mestre sol·licite entre missatges. Això permet que un dispositiu mestre envie múltiples sol·licituds mentre té el control. El valor per defecte és vertader.

### Sintaxi

`Wire.requestFrom(direcció, quantitat)`  
`Wire.requestFrom(direcció, quantitat, parada)`  

### Paràmetres

`adreça`: la direcció esclava de 7 bits del dispositiu per a sol·licitar bytes.  
`quantitat`: el nombre de bytes a sol·licitar.  
`parada`: vertader o fals. true enviarà un missatge de parada després de la sol·licitud, alliberant el bus. False enviarà contínuament un reinici després de la sol·licitud, mantenint la connexió activa.  

### Devolucions

 byte: el nombre de bytes retornats des del dispositiu perifèric.

### Vegeu també

LLENGUATGE [Wire](../wire.md)  
LLENGUATGE [Funcions](../../../Funcions.md)

