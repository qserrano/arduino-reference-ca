
| títol | categoria  | subcategoria | subfunció |
| :---: | :--------: | :----------: | :-------: |
| Mouse.move() | Funcions | USB | Mouse |

# Mouse.move()

### Descripció

Mou el cursor en un ordinador connectat. El moviment a la pantalla sempre és relatiu a la ubicació actual del cursor. Abans d'utilitzar `Mouse.move()` heu de cridar `Mouse.begin()`.

### Sintaxi

* `Mouse.move(xVal, yVal, wheel)`

### Paràmetres

* `xVal`: quantitat a moure al llarg de l'eix x. Tipus de dades permesos: caracter signat.
* `yVal`: quantitat a moure al llarg de l'eix y. Tipus de dades permesos: caracter signat.
* `wheel`: quantitat per moure la roda de desplaçament. Tipus de dades permesos: caracter signat.

### Devolucions

Res

### Exemple de codi

```
#include <Mouse.h>

const int xAxis = A1;         //analog sensor for X axis
const int yAxis = A2;         // analog sensor for Y axis

int range = 12;               // output range of X or Y movement
int responseDelay = 2;        // response delay of the mouse, in ms
int threshold = range / 4;    // resting threshold
int center = range / 2;       // resting position value
int minima[] = {1023, 1023};  // actual analogRead minima for {x, y}
int maxima[] = {0, 0};        // actual analogRead maxima for {x, y}
int axis[] = {xAxis, yAxis};  // pin numbers for {x, y}
int mouseReading[2];          // final mouse readings for {x, y}


void setup() {
  Mouse.begin();
}

void loop() {
  // read and scale the two axes:
  int xReading = readAxis(0);
  int yReading = readAxis(1);

  // move the mouse:
  Mouse.move(xReading, yReading, 0);
  delay(responseDelay);
}

/*
  reads an axis (0 or 1 for x or y) and scales the
  analog input range to a range from 0 to <range>
*/

int readAxis(int axisNumber) {
  int distance = 0; // distance from center of the output range

  // read the analog input:
  int reading = analogRead(axis[axisNumber]);

  // of the current reading exceeds the max or min for this axis,
  // reset the max or min:
  if (reading < minima[axisNumber]) {
    minima[axisNumber] = reading;
  }
  if (reading > maxima[axisNumber]) {
    maxima[axisNumber] = reading;
  }

  // map the reading from the analog input range to the output range:
  reading = map(reading, minima[axisNumber], maxima[axisNumber], 0, range);

  // if the output reading is outside from the
  // rest position threshold,  use it:
  if (abs(reading - center) > threshold) {
    distance = (reading - center);
  }

  // the Y axis needs to be inverted in order to
  // map the movemment correctly:
  if (axisNumber == 1) {
    distance = -distance;
  }

  // return the distance for this axis:
  return distance;
}
```

### Notes i advertències

Quan utilitzeu l'ordre `Mouse.move()`, l'Arduino es fa càrrec del vostre ratolí! Assegureu-vos que teniu el control abans d'utilitzar l'ordre. Un polsador per canviar l'estat de control del ratolí és efectiu.

### Vegeu també

* LLENGUATGE [Mouse](../Mouse.md)
