# Investigación sobre Circuitos Lógicos Secuenciales

## Introducción

En el diseño digital, los **Circuitos Lógicos Secuenciales (CLS)** son fundamentales para implementar sistemas que dependen no solo de las entradas actuales, sino también del historial de estados anteriores. A diferencia de los circuitos combinacionales, los CLS incluyen elementos de memoria que permiten almacenar información y tener un comportamiento basado en el tiempo. Estos circuitos son esenciales en sistemas donde se requiere sincronización y temporización precisa, como en controladores, contadores y máquinas de estado.

### Definición de Circuitos Lógicos Secuenciales (CLS)

Un **Circuito Lógico Secuencial (CLS)** es un tipo de circuito digital en el que las salidas dependen tanto de las entradas actuales como del estado anterior del sistema. Estos circuitos tienen **memoria**, lo que significa que pueden "recordar" información pasada, lo que les permite generar salidas basadas en secuencias de eventos en lugar de únicamente en el estado actual de las entradas.

### Necesidad de Memoria y Sincronización

En muchos sistemas digitales, como los sistemas de control y comunicación, es crucial no solo procesar las entradas actuales, sino también tener en cuenta los eventos previos para tomar decisiones adecuadas. Aquí es donde los CLS juegan un papel fundamental, ya que permiten:

- **Memoria**: Almacenar estados anteriores que influyen en el comportamiento futuro del sistema.
- **Sincronización**: Asegurar que los cambios en las salidas ocurran en momentos precisos, lo que es esencial en sistemas que operan en ciclos de reloj.

### Latches y Flip-Flops

Los **Latches** y **Flip-Flops** son los bloques básicos de construcción de los circuitos secuenciales. Ambos dispositivos almacenan un bit de información, pero difieren en la manera en que responden a las señales de control y temporización.

- **Latch**: Es un dispositivo de almacenamiento de nivel. Su salida cambia cuando la señal de control está activa, es decir, es sensible al nivel de la señal (actúa en tiempo real mientras la señal esté activa).
  - **Latch SR**: Permite almacenar y borrar datos a través de las entradas "Set" y "Reset".
  - **Latch D**: Suprime el comportamiento incierto del Latch SR al tener una sola entrada de datos.

- **Flip-Flop**: A diferencia del latch, el flip-flop es un dispositivo de borde, lo que significa que cambia su estado solo en el borde (flanco) de la señal de reloj, garantizando sincronización con el sistema.
  - **Flip-Flop SR**: Similar al latch SR, pero controlado por el reloj.
  - **Flip-Flop D**: Su salida sigue la entrada de datos "D" en cada flanco de reloj.
  - **Flip-Flop JK**: Una versión mejorada del SR, que evita estados indeterminados y ofrece una funcionalidad más versátil.
  - **Flip-Flop T**: Cambia su estado cada vez que recibe un pulso de reloj, utilizado en contadores.

### Máquinas de Estados Finitos

Las **Máquinas de Estados Finitos (FSM)** son un tipo de CLS que se utiliza para modelar sistemas que pueden estar en uno de varios estados y cambiar de estado en respuesta a las entradas. Existen dos tipos principales de FSM:

- **Máquina de Mealy**: En este tipo de FSM, la salida depende de las entradas actuales y del estado actual del sistema. Los cambios en la entrada pueden afectar inmediatamente la salida.
  
- **Máquina de Moore**: En este caso, las salidas dependen únicamente del estado actual, y no de las entradas directamente. Esto asegura que las salidas solo cambian cuando hay una transición de estado, haciendo que las FSM de Moore sean más estables.

### Análisis de Circuitos Secuenciales

El **análisis** de circuitos secuenciales implica observar su comportamiento mediante el uso de tablas de estados y diagramas de transición. El proceso comienza determinando cómo las entradas afectan el estado del circuito, y cómo ese estado influye en las salidas. Un análisis típico incluye:

1. **Tabla de estados**: Muestra todos los posibles estados y las salidas correspondientes para cada combinación de entradas.
2. **Diagrama de estados**: Representa gráficamente los estados y las transiciones entre ellos.
3. **Tabla de verdad**: Relaciona las entradas y las salidas, similar a los circuitos combinacionales.

### Síntesis de Circuitos Secuenciales

La **síntesis** de circuitos secuenciales implica diseñar el circuito a partir de una especificación dada. Los objetivos principales son minimizar la cantidad de **biestables** (flip-flops) necesarios para almacenar el estado, y optimizar las transiciones entre estados.

- **Mínimo número de biestables**: Para un FSM con 'n' estados, se requieren al menos ⌈log2(n)⌉ flip-flops. La síntesis adecuada debe reducir el número de biestables sin perder funcionalidad.
- **Un biestable por estado**: En algunos diseños, se opta por asignar un flip-flop para cada estado del sistema, lo que simplifica las transiciones a expensas de usar más flip-flops.

### Timing en Circuitos Secuenciales

El **timing** es crucial en los circuitos secuenciales, ya que asegura que las operaciones ocurran de manera sincronizada con el reloj del sistema. Los aspectos de timing más importantes son:

- **Tiempo de configuración (setup time)**: Es el tiempo mínimo que una entrada debe estar estable antes del flanco de reloj.
- **Tiempo de retención (hold time)**: Es el tiempo mínimo que una entrada debe permanecer estable después del flanco de reloj.
- **Tiempo de propagación**: Es el tiempo que tarda una señal en propagarse a través del circuito.
  
Un diseño de CLS eficiente debe tener en cuenta estos tiempos para evitar errores de sincronización y asegurar que el circuito funcione de manera confiable.

