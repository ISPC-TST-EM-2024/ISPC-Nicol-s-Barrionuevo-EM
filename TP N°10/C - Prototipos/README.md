# ¿Qué es la Palabra de Configuración?

La palabra de configuración en un microcontrolador es una serie de bits que define la configuración del hardware del dispositivo. Estos bits controlan aspectos fundamentales como:

**Fuente de reloj**  
**Protección de código**  
**Opciones de arranque**  
**Modos de depuración**  
**Opciones de memoria**

Cada microcontrolador tiene su propio conjunto de bits de configuración, que pueden variar dependiendo del modelo y del fabricante.

## ¿Para Qué Sirve la Palabra de Configuración?

La palabra de configuración sirve para personalizar el comportamiento del microcontrolador según las necesidades específicas de la aplicación. Al configurar estos bits, se pueden habilitar o deshabilitar ciertas funciones del microcontrolador, optimizando su funcionamiento y asegurando que cumpla con los requisitos del proyecto.

**Ejemplos de Configuración:**

Fuente de Reloj: Selección entre un cristal externo, un oscilador interno o un reloj RC.

Protección de Código: Habilitar o deshabilitar la protección de lectura/escritura del código almacenado en la memoria del microcontrolador.

Modos de Arranque: Configuración del modo de arranque, como el arranque desde la memoria flash o desde una memoria externa.

### Tipos de Fusibles en Microcontroladores

Los fusibles en microcontroladores son configuraciones permanentes o semipermanentes que controlan varias características del dispositivo. A continuación, se detallan los tipos más comunes de fusibles:

**1. Fusibles de Configuración de Reloj:**  
Estos fusibles determinan la fuente de reloj del microcontrolador. Ejemplos incluyen:

Oscilador de cristal externo  
Oscilador RC interno  
Reloj de baja frecuencia

**2. Fusibles de Protección de Código:**  
Controlan el acceso a la memoria del microcontrolador, protegiendo el código contra lectura o escritura no autorizada.

**3. Fusibles de Voltaje:**

Configuran los niveles de voltaje necesarios para la operación del microcontrolador.

**4. Fusibles de Watchdog Timer:**

Habilitan o deshabilitan el temporizador de watchdog, que se utiliza para reiniciar el microcontrolador en caso de que se quede bloqueado.

**5. Fusibles de Modo de Depuración:**

Determinan si el microcontrolador puede entrar en un modo de depuración, permitiendo la inspección y modificación del estado interno durante el desarrollo y pruebas.

### Código de Ejemplo

\_\_CONFIG \_CP_OFF & \_CPD_OFF & \_LVP_OFF & \_BODEN_ON & \_MCLRE_OFF & \_PWRTE_ON & \_WDTE_OFF & \_INTOSC_OSC_NOCLKOUT

**Explicación de la Configuración**

→ CP_OFF: Desactiva la protección del código, permitiendo que el código del programa pueda ser leído.

→ CPD_OFF: Desactiva la protección de datos en la EEPROM, permitiendo la lectura y escritura.

→ LVP_OFF: Desactiva la programación de bajo voltaje, requiriendo un alto voltaje para programar el microcontrolador.

→ BODEN_ON: Habilita el detector de fallo de alimentación (Brown-out), que reinicia el microcontrolador si el voltaje cae por debajo de un nivel seguro.

→ MCLRE_OFF: Desactiva la función del pin MCLR, permitiendo usarlo como un pin de entrada/salida general.

→ PWRTE_ON: Habilita el temporizador de encendido, retrasando el arranque del microcontrolador hasta que la fuente de alimentación se estabilice.

WDTE_OFF: Desactiva el temporizador watchdog, que reinicia el microcontrolador si no se restablece periódicamente.

INTOSC_OSC_NOCLKOUT: Configura el uso del oscilador interno sin salida de reloj externa.
