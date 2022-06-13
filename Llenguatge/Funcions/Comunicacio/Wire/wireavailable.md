
| títol | descripció   | categoria  | subcategoria        |
| :---: | :----------: | :--------: | :-----------------: |
| Wire.available() | | Funcions | Comunicació |

# available()

### Descripció

Aquesta funció retorna el nombre de bytes disponibles per a la recuperació amb `read()`. Aquesta funció s'ha de cridar en un dispositiu controlador després d'una crida a `requestFrom()` o en un perifèric dins del controlador `onReceive()`. `available()` hereta de la classe d'utilitat Stream.

### Sintaxi

* `Wire.available()`

### Paràmetres

* Cap.

### Devolucions

El nombre de bytes disponibles per a la lectura.

### Vegeu també

* LLENGUATGE [Wire](../wire.md)
* LLENGUATGE [Funcions](../../Funcions.md)
