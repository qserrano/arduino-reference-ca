
| títol | descripció   | categoria  | subcategoria        |
| :---: | :----------: | :--------: | :-----------------: |
| if(Serial) | | Funcions | Comunicació |

# if(Serial)

### Descripció

Indica si el port especificat (Serial) està llest.

En les plaques amb USB natiu, `if(Serial)` (o `if(SerialUSB)` en Due) indica si la connexió serie USB CDC està oberta o no. Per a totes les altres plaques i els ports CDC que no són USB, això sempre serà vertader.

Això es va introduir en Arduino IDE 1.0.1.

### Sintaxi

*  `if(serial)`

### Paràmetres

*  Cap

### Devolucions

Retorna vertader si el port serie especificat està disponible. Això només retornarà fals si consulta la connexió en sèrie USB CDC de Leonardo abans que estiga llesta. Tipus de dada: booleà.

### Codi d'exemple
```
void setup()
{
  //Inicialitza serial i espera a que el port s'òbriga
  Serial.begin(9600);
  while (!Serial)
  {
    ; // esperar que es connecte el port serie. Necessari per a USB natiu
  }
}

void loop()
{
 // procedeix normalment
}
```

### Vegeu també

*  LLENGUATGE [Serial](../Serial.md)  
*  LLENGUATGE [Funcions](../../Funcions.md)
