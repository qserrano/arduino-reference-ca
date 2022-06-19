---
títol: "int"
categories: [ "Variables" ]
subcategories: [ "Tipus de dades" ]
---

# int

## Descripció

Els nombres enters són el seu tipus de dades principal per a l'emmagatzematge de números.

En Arduino UNO (i altres plaques basades en ATmega), un int emmagatzema un valor de 16 bits (2 bytes). Això produeix un rang de -32,768 a 32,767 (valor mínim de -2^15 i valor màxim de (2^15) - 1). En les plaques basades en Arduino Due i SAMD (com MKR1000 i Zero), un int emmagatzema un valor de 32 bits (4 bytes). Això produeix un rang de -2,147,483,648 a 2,147,483,647 (valor mínim de -2^31 i valor màxim de (2^31) - 1).

int emmagatzema números negatius amb una tècnica anomenada (matemàtiques de complement a 2). El bit més alt, a vegades denominat bit de "signe", marca el número com un número negatiu. La resta dels bits s'inverteixen i se suma 1.

L'Arduino s'encarrega de manejar els números negatius per vosté, perquè les operacions aritmètiques funcionen de manera transparent de la manera esperada. No obstant això, pot haver-hi una complicació inesperada en tractar amb l'operador de desplaçament de bits a la dreta (>>).

## Sintaxi

`int var = valor;`

## Paràmetres

`var`: nom de la variable.  
`val`: el valor que assignes a aqueixa variable.

## Codi d'exemple

Aquest codi crea un nombre enter anomenat 'countUp', que inicialment s'estableix com el número 0 (zero). La variable puja en 1 (un) cada llaç, mostrant-se en el monitor serial.

```
int countUp = 0;            //creates a variable integer called 'countUp'

void setup() {
  Serial.begin(9600);       // use the serial port to print the number
}

void loop() {
  countUp++;                //Adds 1 to the countUp int on every loop
  Serial.println(countUp);  // prints out the current state of countUp
  delay(1000);
}
```

## Notes i Advertiments

Quan es fa que les variables amb signe excedisquen la seua capacitat màxima o mínima, es desborden. El resultat d'un desbordament és impredictible, per la qual cosa ha d'evitar-se. Un símptoma típic d'un desbordament és la "bolcada" de la variable des de la seua capacitat màxima fins a la seua mínima o viceversa, però no sempre és així. Si desitja aquest comportament, use int sense signar.

## Veure també

LLENGUATGE [Constants enteres](../Constants/constants-enteres.md)  
LLENGUATGE [Variables](../../Variables.md)
