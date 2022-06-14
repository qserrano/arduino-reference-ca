---
títol: "&&"
descripció: "and lògic"
categoria: "Estructura"
subcategoria: "Operadors booleans"
---

# &&

### Descripció

L'AND lògic només resulta cert si els dos operands són certs.

### Exemple de codi

Aquest operador es pot utilitzar dins de la condició d'una instrucció if.

```
if (digitalRead(2) == HIGH && digitalRead(3) == HIGH) { // si els DOS interruptors llegeixen HIGH
   // declaracions
}
```

### Notes i advertències

Assegureu-vos de no confondre l'operador AND booleà, && (ampersand doble) amb l'operador AND bit a bit & (ampersand únic). Són bèsties completament diferents.

### Vegeu també

LLENGUATGE [& (bit a bit AND)](../Operadors-bitabit/bitabitand.md)  
LLENGUATGE [Estructura](../../Estructura.md)  
