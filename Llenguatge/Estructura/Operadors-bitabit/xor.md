---
títol: "^"
descripció: "or exclusiu bit a bit"
categoria: "Estructura"
subcategoria: "Operadors bit a bit"
---

# ^

### Descripció

Hi ha un operador una mica inusual en C++ anomenat OR EXCLUSIU per bits, també conegut com XOR per bits. (En anglès, normalment es pronuncia "eks-or".) L'operador XOR bit a bit s'escriu utilitzant el símbol de cursor ^. Una operació XOR per bits dóna com a resultat un 1 només si els bits d'entrada són diferents, en cas contrari resulta un 0.

Precisament,

```
0 0 1 1 operand1
0 1 0 1 operand2
----------
0 1 1 0 (operand1 ^ operand2) - resultat retornat
```

### Exemple de codi

```
int x = 12; // binari: 1100
int y = 10; // binari: 1010
int z = x ^ y; // binari: 0110 o decimal 6
```

L'operador ^ s'utilitza sovint per canviar (és a dir, canviar de 0 a 1, o d'1 a 0) alguns dels bits d'una expressió entera. En una operació XOR per bits, si hi ha un 1 al bit de màscara, aquest bit s'inverteix; si hi ha un 0, el bit no s'inverteix i es manté igual.

```
// Nota: aquest codi utilitza registres específics dels microcontroladors AVR (Uno, Nano, Leonardo, Mega, etc.)
// no es compilarà per a altres arquitectures
void setup() {
  DDRB = DDRB | 0b00100000; // estableix PB5 (pin 13 a Uno/Nano, pin 9 a Leonardo/Micro, pin 11 a Mega) com a SORTIDA
  Serial.begin(9600);
}

void loop() {
  PORTB = PORTB ^ 0b00100000; // inverteix PB5, deixa els altres sense tocar
  retard (100);
}
```

### Vegeu també

EXEMPLE [Tutorial BitMath](https://www.arduino.cc/playground/Code/BitMath)  
LLENGUATGE [Estructura](../../Estructura.md)  
