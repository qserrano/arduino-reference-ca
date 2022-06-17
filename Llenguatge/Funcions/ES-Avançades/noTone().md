---
títol: "noTone()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Avançades"
---

# noTone()

### Descripció

Deté la generació d'una ona quadrada desencadenada per `tone()`. No té efecte si no es genera cap to.

### Sintaxi

`noTone(pin)`

### Paràmetres

`pin`: el pin d'Arduino en el qual deixar de generar el to

### Devolucions

Res

### Notes i Advertiments

Si desitja tocar diferents tons en diversos pins, ha de cridar a `noTone()` en un pin abans de cridar a `tone()` en el següent pin.

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
