
| títol | descripció   | categoria  | subcategoria        |
| :---: | :----------: | :--------: | :-----------------: |
| Wire.onReceive() | | Funcions | Comunicació |

# onReceieve()

### Descripció

Aquesta funció registra una funció que cal cridar quan un dispositiu perifèric rep una transmissió d'un dispositiu controlador.

### Sintaxi

* `Wire.onReceive(handler)`

### Paràmetres

* `handler`: la funció que cal cridar quan el dispositiu perifèric rep dades; això hauria de prendre un sol paràmetre int (el nombre de bytes llegits des del dispositiu controlador) i no retornar res.

### Devolucions

Cap.

### Vegeu també

* LLENGUATGE [Wire](../wire.md)
* LLENGUATGE [Funcions](../../Funcions.md)

