---
títol: "analogReference()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Analogiques"
---

# analogReference()

### Descripció

Configura el voltatge de referència utilitzat per a l'entrada analògica (és a dir, el valor utilitzat com la part superior del rang d'entrada). Les opcions són:
- Plaques Arduino AVR (UNO, Mega, Leonardo, etc.)
  - DEFAULT: la referència analògica predeterminada de 5 volts (en plaques Arduino de 5 V) o 3,3 volts (en plaques Arduino de 3,3 V)
  - INTERN: una referència incorporada, igual a 1,1 volts en ATmega168 o ATmega328P i 2,56 volts en ATmega32U4 i ATmega8 (no disponible en Arduino Mega)
  - INTERNAL1V1: una referència de 1.1V incorporada (només Arduino Mega)
  - INTERNAL2V56: una referència integrada de 2,56 V (només Arduino Mega)
  - EXTERN: el voltatge aplicat al pin AREF (només 0 a 5V) s'usa com a referència.
- Plaques Arduino SAMD (Zero, etc.)
  - AR_DEFAULT: la referència analògica predeterminada de 3,3 V
  - AR_INTERNAL: una referència de 2,23 V incorporada
  - AR_INTERNAL1V0: una referència de 1,0 V incorporada
  - AR_INTERNAL1V65: una referència de 1,65 V incorporada
  - AR_INTERNAL2V23: una referència de 2,23 V incorporada
  - AR_EXTERNAL: el voltatge aplicat al pin AREF s'usa com a referència
- Plaques Arduino megaAVR (Un Wifi Rev2)
  - PREDETERMINAT: una referència de 0,55 V incorporada
  - INTERN: una referència de 0,55 V incorporada
  - VDD: Vdd de l'ATmega4809. 5V en l'Un Wifi Rev2
  - INTERNAL0V55: una referència de 0,55 V incorporada
  - INTERNAL1V1: una referència de 1,1 V integrada
  - INTERNAL1V5: una referència de 1,5 V integrada
  - INTERNAL2V5: una referència de 2,5 V integrada
  - INTERNAL4V3: una referència de 4,3 V incorporada
  - EXTERN: el voltatge aplicat al pin AREF (només 0 a 5V) s'usa com a referència
- Plaques Arduino SAM (per venciment)
  - AR_DEFAULT: la referència analògica predeterminada de 3,3 V. Aquesta és l'única opció admesa per al venciment.
- Arduino Mbed US Nano Boards (Nano 33 BLE), Arduino Mbed US Edge Boards (Edge Control)
  - AR_VDD: la referència predeterminada de 3,3 V
  - AR_INTERNAL: referència de 0,6 V incorporada
  - AR_INTERNAL1V2: referència de 1,2 V (referència interna de 0,6 V amb guany 2x)
  - AR_INTERNAL2V4: referència de 2,4 V (referència interna de 0,6 V amb guany 4x)

### Sintaxi

`analogReference(type)`

### Paràmetres

`type`: quin tipus de referència usar (veure llista d'opcions en la descripció).

### Devolucions

Res

### Notes i Advertiments

Després de canviar la referència analògica, les primeres lectures d'`analogRead()` poden no ser precises.

No use menys de 0 V ni més de 5 V per al voltatge de referència extern en el pin AREF! Si està utilitzant una referència externa en el pin AREF,
ha d'establir la referència analògica en EXTERNA abans de cridar a `analogRead()`. En cas contrari, curtcircuitarà el voltatge de referència actiu
(generat internament) i el pin AREF, possiblement danyant el microcontrolador en la seua placa Arduino.

Alternativament, pot connectar el voltatge de referència extern al pin AREF a través d'una resistència de 5K, la qual cosa li permet canviar entre
voltatges de referència interns i externs. Tinga en compte que la resistència alterarà el voltatge que s'usa com a referència perquè hi ha una resistència
interna de 32K en el pin AREF. Els dos actuen com un divisor de voltatge, per la qual cosa, per exemple, 2,5 V aplicats a través de la resistència produiran
2,5 * 32 / (32 + 5) = ~2,2 V en el pin AREF.

### Veure també

EXEMPLE [Descripció dels pins d'entrada analògica (en anglés)](http://arduino.cc/en/Tutorial/AnalogInputPins)  
LLENGUATGE [Funcions](../../Funcions.md)
