---
títol: "tone()"
descripció: ""
categoria: "Funcions"
subcategoria: "ES Avançades"
---

## tone()

### Descripció

Genera una ona quadrada de la freqüència especificada (i un cicle de treball del 50%) en un pin. Es pot especificar una duració; en cas contrari, l'ona continua fins que es diu a `noTone()`. El pin es pot connectar a un brunzidor piezoelèctric o un altre altaveu per a reproduir tons.

Només es pot generar un to alhora. Si ja s'està reproduint un to en un pin diferent, la crida a `tone()` no tindrà efecte. Si el to es reprodueix en el mateix pin, la crida establirà la seua freqüència.

L'ús de la funció `tone()` interferirà amb l'eixida PWM en els pins 3 i 11 (en plaques que no siguen Mega).

No és possible generar tons inferiors a 31Hz. Per a obtindre detalls tècnics, consulte les notes de [Brett Hagman](https://github.com/bhagman/Tone#ugly-details).

### Sintaxi

`tone(pin, frequency)`  
`tone(pin, frequency, duration)`  

### Paràmetres

`pin`: el pin Arduino en el qual generar el to.  
`frequency`: la freqüència del to en hertzs. Tipus de dades permeses: unsigned int  
`duration`: la duració del to en mil·lisegons (opcional). Tipus de dades permeses: unsigned long  

### Devolucions

Res

### Notes i Advertiments

Si desitja tocar diferents tons en diversos pins, ha de cridar a `noTone()` en un pin abans de cridar a `tone()` en el següent pin.

### Veure també

LLENGUATGE [Funcions](../../Funcions.md)
