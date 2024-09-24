# Investigación : Álgebra de Boole, Circuitos Digitales y Circuitos Lógicos Combinacionales

## Álgebra de Boole

El **Álgebra de Boole** es un sistema matemático que trabaja con valores binarios, principalmente 0 y 1, y es la base para la lógica digital utilizada en el diseño de circuitos electrónicos y sistemas de control. Este tipo de álgebra utiliza operaciones lógicas como:

- **AND (y)**: La operación AND solo es verdadera cuando todas sus entradas son verdaderas.
  - Notación: A ∧ B o A • B
  - Tabla de verdad: 
    | A | B | A ∧ B |
    |---|---|-------|
    | 0 | 0 |   0   |
    | 0 | 1 |   0   |
    | 1 | 0 |   0   |
    | 1 | 1 |   1   |
  
- **OR (o)**: La operación OR es verdadera si al menos una de las entradas es verdadera.
  - Notación: A ∨ B o A + B
  - Tabla de verdad:
    | A | B | A ∨ B |
    |---|---|-------|
    | 0 | 0 |   0   |
    | 0 | 1 |   1   |
    | 1 | 0 |   1   |
    | 1 | 1 |   1   |

- **NOT (negación)**: La operación NOT invierte el valor de la entrada, es decir, convierte 1 en 0 y 0 en 1.
  - Notación: ¬A o A'
  - Tabla de verdad:
    | A | ¬A |
    |---|----|
    | 0 |  1 |
    | 1 |  0 |

### Propiedades del Álgebra de Boole

1. **Ley conmutativa**: A + B = B + A, A • B = B • A
2. **Ley asociativa**: (A + B) + C = A + (B + C), (A • B) • C = A • (B • C)
3. **Ley distributiva**: A • (B + C) = A • B + A • C, A + (B • C) = (A + B) • (A + C)
4. **Ley de identidad**: A + 0 = A, A • 1 = A
5. **Ley de complemento**: A + A' = 1, A • A' = 0

El Álgebra de Boole se utiliza para simplificar expresiones lógicas, lo que facilita el diseño y optimización de circuitos digitales.

## Circuitos Digitales

Los **Circuitos Digitales** son sistemas electrónicos que procesan y transmiten información a través de señales binarias. Estas señales solo pueden tener dos valores posibles: **0 (bajo)** o **1 (alto)**, representando el estado de apagado o encendido, respectivamente. Los circuitos digitales son fundamentales en la informática, telecomunicaciones y automatización.

### Características de los Circuitos Digitales

- **Bajo ruido**: Los circuitos digitales son menos propensos al ruido en comparación con los circuitos analógicos, lo que les permite funcionar de manera precisa.
- **Fiabilidad**: Al trabajar con solo dos estados (0 y 1), los circuitos digitales son más resistentes a las interferencias y errores.
- **Modularidad**: Pueden construirse combinando varios componentes básicos, como compuertas lógicas, para realizar funciones más complejas.

Los circuitos digitales se clasifican en dos categorías principales:

1. **Circuitos Combinacionales**: Las salidas dependen únicamente de las entradas actuales.
2. **Circuitos Secuenciales**: Las salidas dependen de las entradas actuales y del estado previo, involucrando elementos de memoria como flip-flops.

## Circuitos Lógicos Combinacionales

Los **Circuitos Lógicos Combinacionales** son un tipo de circuito digital en el cual la salida es una función lógica de sus entradas actuales. No tienen memoria y, por lo tanto, no dependen de entradas pasadas. Los circuitos combinacionales se utilizan para realizar operaciones lógicas, matemáticas y de control en sistemas digitales.

### Ejemplos de Circuitos Combinacionales

1. **Sumador**: Un circuito que realiza la operación de suma entre dos números binarios.
2. **Multiplexor (MUX)**: Un circuito que selecciona una de varias señales de entrada y la pasa a la salida.
3. **Comparador**: Un circuito que compara dos números binarios y determina si uno es mayor, menor o igual al otro.
4. **Codificador y decodificador**: Circuitos que traducen de un formato de código binario a otro (codificación) o viceversa (decodificación).

### Diseño de Circuitos Combinacionales

El diseño de un circuito combinacional implica los siguientes pasos:

1. **Definir la función lógica**: Describir cómo las entradas afectan las salidas en función de una tabla de verdad.
2. **Obtener la expresión lógica**: A partir de la tabla de verdad, se extrae la expresión lógica que define el circuito.
3. **Simplificación**: La expresión lógica puede ser simplificada utilizando el álgebra de Boole o un mapa de Karnaugh para reducir el número de compuertas necesarias.
4. **Implementación**: Finalmente, la expresión simplificada se implementa usando compuertas lógicas (AND, OR, NOT, etc.).

### Mapa de Karnaugh

El **mapa de Karnaugh** es una herramienta gráfica utilizada para simplificar expresiones lógicas de manera eficiente. Organiza las combinaciones de entradas en una tabla y permite identificar patrones visuales que facilitan la reducción de términos.

---

**Referencias**:
- "Sistemas Digitales" de Ronald Tocci y Neal Widmer.
- "Diseño Digital" de M. Morris Mano.
- "Álgebra de Boole y Circuitos Combinatorios" de Oscar Miguel Villegas.
