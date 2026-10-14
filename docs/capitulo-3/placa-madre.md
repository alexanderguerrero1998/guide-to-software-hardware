# Capítulo 3. En la placa madre

> Traducción al español del Capítulo 3 («On the Motherboard») de *Complete A+ Guide to IT Hardware and Software: CompTIA A+ Exams 220-1101 & 220-1102* (Cheryl A. Schmidt, Christopher Lee) — material de estudio de uso personal.
>
> Nota: las figuras y las tablas del libro son imágenes y no se incluyen aquí; se conserva su leyenda traducida como referencia.

En este capítulo aprenderás:

- Cómo reconocer e identificar las partes importantes de la placa madre
- Lo básico de cómo funciona un procesador
- Cuestiones a considerar al actualizar o reemplazar una placa madre o un procesador
- Información sobre las GPU
- Cómo agregar tarjetas a las computadoras
- Las diferencias entre los adaptadores y ranuras PCI, AGP y PCIe
- Tecnologías de la placa madre como HyperTransport, Hyperthreading y multinúcleo
- Los factores de forma y las opciones de seguridad de la placa madre
- Los síntomas de problemas de placa madre y CPU
- Los beneficios de la escucha activa

**Objetivos del examen CompTIA:**

- 1101-3.4 Dado un escenario, instalar y configurar placas madre, unidades centrales de procesamiento (CPU) y tarjetas adicionales.
- 1101-5.2 Dado un escenario, diagnosticar problemas relacionados con placas madre, RAM, CPU y energía.
- 1102-4.7 Dado un escenario, usar técnicas de comunicación y profesionalismo adecuados.

## Introducción a la placa madre

La placa madre contiene la mayor parte de la electrónica, está presente en la mayoría de los dispositivos electrónicos, incluidas las computadoras, y es importante para cualquier tipo de dispositivo. La Figura 3.1 muestra algunos de los componentes clave de la placa madre que cubriremos.

> Figura 3.1 Componentes clave de la placa madre

## Descripción general del procesador

En el corazón de toda computadora está el **procesador**, que determina, en gran medida, la potencia de la computadora. El procesador también se llama **unidad central de procesamiento (CPU)** o **microprocesador**. El procesador ejecuta instrucciones, realiza cálculos y coordina operaciones de entrada/salida. Cada placa madre tiene chips que trabajan con la CPU y que están diseñados según especificaciones exactas. Los principales fabricantes de procesadores hoy son Intel, Motorola, VIA, Samsung, NVIDIA, Apple Inc., Qualcomm y AMD (Advanced Micro Devices, Inc.). Intel y AMD son los fabricantes predominantes de procesadores para computadoras de escritorio y portátiles. Un término que podrías escuchar relacionado con las CPU de Intel y AMD es **x86-64**. El x86 se relaciona con el procesador Intel 8086, y el 64, o x64, refleja la actualización a una versión de 64 bits. Intel tiene su propia arquitectura de CPU patentada llamada Intel 64, y AMD tiene la arquitectura patentada AMD64.

Los **procesadores ARM** se usan en dispositivos móviles como teléfonos inteligentes, tabletas y portátiles. ARM solía ser un acrónimo de Acorn RISC (*reduced instruction set computing*) Machine y luego Advanced RISC Machines, pero hoy es solo una arquitectura usada en procesadores y microcontroladores. Los procesadores ARM pueden ser de 32 o 64 bits y se usan con frecuencia en dispositivos móviles como teléfonos inteligentes, tabletas, cámaras digitales y portátiles, pero también se pueden usar en computadoras de escritorio y servidores. Los procesadores ARM consumen menos energía, producen menos calor y cuestan menos que los procesadores de AMD o Intel. La empresa Arm Ltd. también licencia sus propios diseños a otras empresas que crean sus propios productos.

Una placa madre acepta los procesadores de uno o más fabricantes específicos; por ejemplo, una placa madre que acepta un procesador Intel no admitirá un procesador AMD. La Figura 3.2 muestra un procesador.

> Figura 3.2 Procesador Intel

## Fundamentos del procesador

Los procesadores vienen en una variedad de velocidades, medidas en gigahercios (GHz). El hertz es una medida de ciclos por segundo. Un hertz, escrito 1 Hz, equivale a 1 ciclo por segundo. Un gigahercio, o 1 GHz, es 1000 millones de ciclos por segundo. Los procesadores actuales pueden funcionar a velocidades cercanas a 5 GHz.

### Buses

Los procesadores operan con 1s y 0s. Los 1s y 0s deben viajar de un lugar a otro dentro del procesador, así como hacia afuera, a otros chips. Para mover los 1s y 0s, se usan líneas electrónicas llamadas **bus**. Las líneas electrónicas dentro de la CPU se conocen como **bus de datos interno**, o **bus del sistema**. En el Intel 8086 (del cual se originó el término arquitectura x86), el bus de datos interno comprende 16 líneas separadas, y cada línea transporta un solo 1 o un solo 0. En los procesadores actuales, 64 o 128 líneas de bus de datos interno operan de forma concurrente.

Para que una CPU se comunique con dispositivos del mundo exterior, como una impresora, los 1s y 0s viajan por el **bus de datos externo**. El bus de datos externo conecta el procesador con los adaptadores, el teclado, el ratón, el almacenamiento y otros dispositivos. Puedes ver las líneas de datos externas mirando entre las ranuras de expansión de la placa madre. Los procesadores actuales tienen rutas de datos externas de 64 y 128 bits. La Figura 3.3 muestra los buses de datos internos y externos.

> Figura 3.3 Buses de datos internos y externos

### ALU

Un procesador tiene un componente especial llamado **unidad aritmética lógica (ALU)**, que realiza todos los cálculos y la lógica de comparación que necesita la computadora. La Figura 3.3 muestra la idea básica de cómo la ALU se conecta con los registros, la unidad de control y el bus interno. La **unidad de control** coordina las actividades dentro del procesador. La **unidad de E/S** gestiona los datos que entran y salen del procesador. Los **registros** en la CPU constituyen un área de almacenamiento de alta velocidad para los 1s y 0s antes de que los bits sean procesados.

### Procesamiento de datos

Para entender cómo procesa datos una computadora, considera una carta escrita en una computadora que empieza con «QUERIDA MAMÁ». Para la computadora, cada letra del alfabeto es una combinación diferente de ocho 1s y 0s. Por ejemplo, la letra D es 01000100 y la letra E es 01000101. La Figura 3.4 demuestra que el tamaño del bus aumenta enormemente el rendimiento de una computadora, de forma muy parecida a como aumentar el número de carriles de una autopista disminuye la congestión.

> Figura 3.4 Rendimiento del bus

### Pipelines

Los procesadores tienen múltiples **pipelines** (buses internos separados) que operan simultáneamente. Para entender el *pipelining*, toma el ejemplo de un restaurante de comida rápida. En el restaurante, supongamos que hay cinco pasos involucrados en preparar una hamburguesa y entregarla al cliente. Para que este proceso de hamburguesas vaya más rápido, podrías (quizá) hacer una de las cosas que se muestran en la Figura 3.5.

> Figura 3.5 Maneras de obtener procesos más rápidos

Para relacionarlo con los procesadores, podrías aumentar la velocidad de reloj de la CPU, cambiar la estructura del pipeline de la CPU en cuanto a cuántos pasos hay en cada pipeline, y/o hacer que la CPU tenga múltiples pipelines. Por ejemplo, si un procesador tiene dos pipelines, la carta «Querida mamá» puede estar en un pipeline, mientras que la carga de una foto usando otra aplicación puede estar en el otro pipeline.

## Descripción general de cómo acelerar las operaciones del procesador

Puedes determinar la velocidad de un procesador mirando el número de modelo en el chip, pero los procesadores con frecuencia tienen dispositivos conectados para enfriarlos, lo que dificulta ver lo escrito en el chip. Un procesador comúnmente no usa su velocidad máxima todo el tiempo, para ahorrar energía o mantenerse frío. Además, un procesador no siempre funciona a su máximo potencial por muchas razones, incluidos el código usado dentro de una aplicación, el cambio del usuario de una aplicación a otra, un ancho de bus inadecuado o la cantidad de RAM instalada. Un procesador también puede operar por encima de sus especificaciones nominales para manejar periodos de mayor carga de trabajo.

### Consejo técnico: ubicar la velocidad del procesador

Una forma fácil de saber la velocidad del procesador en Windows es ir al Explorador de archivos, hacer clic con el botón derecho en «Este equipo» y seleccionar «Propiedades».

Ya hemos visto cómo aumentar el pipeline de la CPU puede, en cierta medida, mejorar las operaciones del procesador, pero también existen otras tecnologías. Empezamos definiendo algunos de los términos que se relacionan con esta área y asociando esos términos con conceptos y las diversas tecnologías usadas. La Tabla 3.1 enumera algunos términos relacionados con la velocidad.

> Tabla 3.1 Términos de velocidad de la placa madre

| Término | Explicación |
|---|---|
| Reloj o velocidad de reloj (*clock*) | La velocidad del reloj interno del procesador, medida en gigahercios. |
| Front side bus (FSB) | La velocidad (comúnmente llamada velocidad de la placa madre) entre la CPU y algunos de los componentes de la placa madre. A veces se indica en megatransferencias por segundo, o MT/s. Con MT/s no solo se considera la velocidad del FSB, sino también cuántas transferencias del procesador ocurren en cada ciclo de reloj. Un FSB de 266 MHz que puede hacer cuatro transferencias por segundo podría indicarse como 1064 MT/s. |
| Back side bus | La velocidad entre la CPU y la caché L2 ubicada fuera de la CPU principal pero en el mismo chip. |
| Velocidad del bus PCI | La velocidad usada para entregar datos en el bus PCI. Las velocidades comunes del bus PCI son 33 y 66 MHz, lo que permite anchos de banda de hasta 533 MB/s. |

### Reloj (clocking)

Una placa madre genera una señal de reloj que se usa para controlar la transferencia de 1s y 0s hacia y desde el procesador. Un ciclo de reloj va de un punto de la onda senoidal al siguiente punto que se encuentra en el mismo punto de la onda senoidal más adelante en el tiempo. En las computadoras antiguas, los datos se enviaban a la CPU solo una vez durante un ciclo de reloj. Hoy, los datos se envían cuatro veces durante un solo ciclo de reloj, como se muestra en la Figura 3.6.

> Figura 3.6 Ciclo de reloj que sincroniza datos cuatro veces por ciclo

### Caché

Un concepto importante relacionado con la velocidad del procesador es mantener los datos fluyendo hacia el procesador. Los datos o la instrucción que la CPU necesita procesar generalmente se encuentran en uno de cuatro lugares: la memoria caché, la memoria de la placa madre (memoria principal), una unidad de estado sólido (SSD, que también es memoria) o el disco duro. La **memoria caché** es un tipo de memoria muy rápida diseñada para aumentar la velocidad y la eficiencia de las operaciones del procesador. La caché proporciona el acceso más rápido. Si la información no está en la memoria caché, el procesador busca los datos en la RAM de la placa madre. Si la información no está allí, se recupera del disco duro y se coloca en la memoria de la placa madre o en la caché. El acceso al disco duro es el más lento de los tres. La Tabla 3.2 enumera los tipos de caché. La Figura 3.7 muestra la jerarquía de dónde busca los datos la CPU.

> Tabla 3.2 Tipos de caché

| Tipo | Explicación |
|---|---|
| Caché L1 | Memoria caché integrada en el procesador y el tipo más rápido. |
| Caché L2 | Caché en el encapsulado del procesador pero que no forma parte de la CPU; también llamada caché *on-die*. |
| Caché L3 | Normalmente se encuentra en procesadores más potentes y puede ubicarse en la carcasa de la CPU (*on-die*) o en la placa madre. |

> Figura 3.7 Fuentes de datos de la CPU y jerarquía de acceso a datos

### Tecnología de hilos (threading)

Se usan dos técnicas comunes de hilos para acelerar la eficiencia del procesador: el **multithreading** y la **HT (Hyperthreading Technology)**. Un **hilo** (*thread*) es una pequeña pieza de un proceso de aplicación. Un sistema operativo como Windows programa y asigna recursos a un hilo. Cada hilo puede compartir recursos (como el procesador o la memoria caché) con otros hilos. Un hilo en el pipeline podría tener un retraso debido a que espera que se recuperen datos o que se obtenga acceso a un puerto u otro componente de hardware. El multithreading mantiene la línea en movimiento al permitir que otro hilo ejecute algo de código. Esto es como un cajero de supermercado atendiendo a otro cliente mientras alguien va a buscar una barra de pan olvidada. La Figura 3.8 muestra este concepto.

> Figura 3.8 Multithreading

La **HT de Intel** (Hyperthreading, Hyper-Threading o HT Technology) permite que un solo procesador maneje dos conjuntos separados de instrucciones simultáneamente. Para el sistema operativo, la HT hace que el sistema parezca tener múltiples procesadores. Intel afirma que el sistema puede tener hasta un 30 % de aumento en el rendimiento, pero los estudios han demostrado que el aumento depende de la aplicación.

### Conexión con el procesador

Acceder a la caché L2 y a los componentes de la placa madre era un cuello de botella en los sistemas antiguos. La solución a este problema es usar dos buses: un bus del lado posterior (*back side bus*) y un bus del lado frontal (*front side bus*). El **bus del lado posterior** conecta la CPU con la caché L2. El **bus del lado frontal (FSB)** (ver la Figura 3.9) conecta la CPU con los componentes de la placa madre. El bus del lado frontal se considera la velocidad de la placa madre.

> Figura 3.9 Bus del lado frontal y bus del lado posterior

Mucha gente piensa que cuanto mayor es la velocidad de la CPU, más rápida es la computadora. Esto rara vez es cierto. Varios factores contribuyen a la velocidad de una computadora. Un factor es la velocidad del bus. La **velocidad del bus** describe qué tan rápido puede comunicarse la CPU con los componentes de la placa madre, como la memoria, el chipset o el bus PCI/PCIe.

Intel y AMD tienen tecnologías para reemplazar el bus del lado frontal en algunas partes. La solución de AMD es **Direct Connect**. Direct Connect permite que cada uno de los núcleos del procesador se conecte directamente con la memoria, con los demás componentes de la placa madre (como las ranuras de expansión) y con otros núcleos del procesador mediante un bus de alta velocidad llamado **HyperTransport** (ver la Figura 3.11, más adelante en el capítulo). AMD está actualizando HyperTransport a **Infinity Fabric**. Intel tiene **Ultra Path Interconnect (UPI)**, **Serial Peripheral Interface (SPI)** y **Direct Media Interface (DMI)**, que son conexiones punto a punto entre el procesador y uno o más componentes de la placa madre.

### Procesadores multinúcleo

Un **procesador de un solo núcleo** es solo un procesador. Tanto Intel como AMD ofrecen **procesadores multinúcleo**, lo que significa más de una CPU en el mismo encapsulado (ver la Figura 3.11). Cada núcleo puede ejecutar programas o hilos. Un solo Intel Core i9 CPU tiene 18 núcleos, y el AMD Ryzen Threadripper tiene 64 núcleos y 128 hilos. La Figura 3.10 muestra cómo se conectan múltiples procesadores Intel. La Figura 3.11 muestra cómo cada CPU AMD accede a la RAM y dónde se usa el bus HyperTransport para la conectividad.

> Figura 3.10 Arquitectura multinúcleo de Intel

> Figura 3.11 Acceso a memoria cuádruple núcleo de AMD

### Consejo técnico: ¿cuántos núcleos e hilos tienes?

Haz clic con el botón derecho en la barra de tareas de Windows > Administrador de tareas > pestaña Rendimiento > CPU > busca «Núcleos» y «Procesadores lógicos» (hilos).

Un **procesador lógico** puede ejecutar su propio conjunto de instrucciones. Todas las aplicaciones pueden aprovechar la tecnología multinúcleo y los procesos en segundo plano asociados con el sistema operativo y las aplicaciones. Esto mejora las operaciones cuando se hace multitarea o cuando se ejecutan aplicaciones potentes que requieren que se ejecuten muchas instrucciones, como aplicaciones de dibujo y juegos.

## Unidad de procesamiento gráfico (GPU)

Otro cuello de botella para el rendimiento de la computadora es el video. Los usuarios de computadoras que quieren mejor rendimiento de video compran un adaptador de video separado que contiene una **GPU**. Tanto Intel como AMD tienen una **unidad de procesamiento gráfico (GPU)** dentro de la CPU en algunos de sus modelos de procesador. Con una **GPU integrada (iGPU)**, a veces llamada **procesador gráfico integrado (IGP)**, no se requiere una tarjeta de video externa con GPU, y los datos gráficos se procesan rápidamente, con un consumo de energía reducido.

Las CPU actuales contienen procesadores multinúcleo, y las GPU contienen cientos de procesadores de núcleos más pequeños. Las GPU también se pueden usar para otros propósitos que no están directamente relacionados con los gráficos pero que aumentan el rendimiento del sistema. Estas GPU a veces se denominan **GPU de propósito general (GPGPU)**. La Figura 3.12 muestra cómo un IGP está dentro del mismo encapsulado que los núcleos de la CPU.

> Figura 3.12 CPU vs. GPU

AMD llama a sus procesadores que tienen una GPU integrada con la CPU **unidades de procesamiento acelerado (APU)**. Intel llama a su GPU integrada Intel HD Graphics e Intel Iris Graphics.

## Introducción a la virtualización

Una ventaja de tener múltiples núcleos de procesador es que permiten que tanto las computadoras domésticas como las de empresa aprovechen la tecnología virtual. La **virtualización** te permite tener una o más **máquinas virtuales (VM)** en la misma computadora. El software de virtualización, como VMware Workstation, Oracle VM VirtualBox o Microsoft Hyper-V, permite que una computadora actúe como si fuera dos o más computadoras. La computadora puede tener dos o más sistemas operativos instalados mediante el uso del software de virtualización. Cada sistema operativo no tiene conocimiento del o de los otros sistemas operativos en la computadora (ver la Figura 3.13).

> Figura 3.13 El concepto de virtualización

Windows 8, 10 y 11 tienen Hyper-V, que permite que una aplicación se ejecute en un entorno virtual como si se hubiera instalado un sistema operativo más antiguo. Las empresas suelen usar la virtualización para poder usar software heredado en máquinas más nuevas, pero manteniéndolo separado del sistema operativo principal o de otra máquina virtualizada en la misma computadora. La reducción de costos y de espacio físico son beneficios de la virtualización. Los usuarios domésticos pueden instalar múltiples sistemas operativos en VM separadas dentro de la misma caja física, y cada VM se ve como una computadora separada. Para prepararte mejor para los exámenes de certificación CompTIA A+, podrías instalar Windows 10 u 11 y Linux.

Seleccionar una placa madre y un procesador es importante en un entorno virtual. Consulta la documentación del software de virtualización para determinar si la CPU usada es compatible. Asegúrate de habilitar el soporte de virtualización en el firmware (se cubre en el Capítulo 4, «Introducción a la configuración»). Otra cuestión relacionada con los procesadores y la virtualización es la licencia. Para el software de virtualización que debe comprarse (es decir, que no es gratuito), el fabricante del software puede cobrar por procesador o por zócalo (*socket*), o por núcleo.

## Procesadores Intel

Tradicionalmente, Intel clasificaba sus procesadores por GHz, y la gente comparaba los procesadores según la velocidad únicamente. Ahora Intel organiza sus productos por números de familia. Dentro de una familia de procesadores, puedes comparar atributos como la velocidad, la cantidad de memoria caché y otras tecnologías. La Tabla 3.3 muestra las familias de procesadores de Intel. La Figura 3.14 muestra un primer plano de un procesador instalado en una placa madre. La Figura 3.15 muestra cómo descifrar los modelos de procesador Intel.

> Tabla 3.3 Familias de procesadores Intel

| Familia de procesadores* | Comentarios |
|---|---|
| Xeon | CPU para servidores y PC profesionales que necesitan memoria ECC, grandes cantidades de memoria, mayor caché, más núcleos y múltiples sockets. |
| Core X | Procesador de 18 núcleos (al cierre de esta edición) para alto rendimiento, juegos extremos, creación de contenido intensiva y multitarea masiva. |
| Core i9 | Potente procesador multinúcleo para juegos y creación de contenido intensiva, así como multitarea masiva. |
| Core i7 | Multinúcleo con memoria caché compartida entre núcleos y controlador de memoria integrado. Bueno para virtualización, diseño y creación gráfica/multimedia, y juegos. |
| Core i5 | Procesador de gama media de doble y cuádruple núcleo. Se usa para video, fotos, correo electrónico y acceso a internet. |
| Core i3 | Procesador de escritorio y móvil de gama baja usado para tareas comunes como procesamiento de textos y acceso a internet. |

*Intel mejora constantemente sus procesadores. Para obtener más información, visita www.intel.com.

> Figura 3.14 Procesador instalado

> Figura 3.15 Cómo descifrar los números de modelo de los procesadores Intel

## Procesadores AMD

AMD es el mayor rival de Intel en procesadores de computadora. Cualquiera que compre un procesador debe investigar todos los modelos y vendedores. La Tabla 3.4 enumera las familias de procesadores AMD, y la Figura 3.16 muestra cómo interpretar los números de modelo de las CPU AMD.

> Tabla 3.4 Familias de procesadores AMD

| Familia de procesadores | Comentarios |
|---|---|
| Ryzen Threadripper | De 8 a 64 núcleos, 128 hilos de procesamiento y de 20 a 292 MB de caché para procesadores de escritorio de gama extremadamente alta. |
| Ryzen 9 | De 8 a 16 núcleos, 32 hilos de procesamiento y hasta 72 MB de caché. |
| Ryzen 7 | 8 núcleos, 16 hilos de procesamiento, 20 MB de caché para juegos, creación de contenido de alta gama y multitarea masiva. |
| Ryzen 5 | De 4 a 6 núcleos, hasta 12 hilos de procesamiento y hasta 20 MB de caché para uso laboral o doméstico. |
| Ryzen 3 | 4 núcleos y hasta 18 MB de caché para uso informático estándar. |

> Figura 3.16 Cómo descifrar los números de modelo de los procesadores AMD

## Zócalos de CPU

Un procesador se inserta en un **zócalo de CPU** (*CPU socket*). Hay diferentes tipos de zócalos, pero cada zócalo tiene un número específico de pines y solo acepta CPU específicas. Una placa madre que puede llevar más de una CPU aparecerá en la documentación/especificaciones como una placa madre **multizócalo** (*multisocket*). Normalmente, son las placas madre de un servidor, una computadora más potente usada en redes, las que tienen una placa madre multizócalo. La Figura 3.17 muestra el zócalo de CPU de una placa madre de escritorio.

> Figura 3.17 Zócalo de CPU

Los zócalos del procesador también se llaman **zócalos de inserción sin fuerza (ZIF)** (*zero insertion force*) y vienen en diferentes tamaños. Un zócalo ZIF tiene una pequeña palanca al costado que, cuando se levanta, saca un poco el procesador hacia arriba y fuera de los orificios del zócalo. Al instalar un procesador, alineas la CPU sobre el zócalo y presionas la palanca hacia abajo para introducir el procesador en el zócalo con fuerza uniforme. En la Figura 3.17, observa la palanca junto al zócalo que se usa para levantar la cubierta metálica.

### Consejo técnico: comprar la CPU correcta

Si compras una placa madre y un procesador por separado, es importante asegurarte de que el zócalo de CPU de la placa madre sea del tipo correcto para el procesador.

- Zócalos Intel: LGA 1151, 1155, 1156, 1200, 2066, 3647
- Zócalos AMD: AM5, AM4, TR4, TRX4

## Enfriamiento del procesador

Mantener una CPU fría es fundamental. Tanto Intel como AMD tienen tecnologías que reducen el consumo de energía (y el calor) del procesador apagando partes no usadas del procesador o ralentizándolo cuando empieza a sobrecalentarse. Pero estas medidas por sí solas no son suficientes. Los sistemas actuales usan uno o más de los métodos enumerados en la Tabla 3.5. La Figura 3.18 muestra un disipador de calor (*heat sink*) y un ventilador.

> Tabla 3.5 Métodos de enfriamiento del procesador

| Método | Descripción |
|---|---|
| Disipador de calor (*heat sink*) | Un disipador de calor es un bloque de metal (normalmente aluminio o cobre), barras de metal o aletas metálicas que se fijan a la parte superior del procesador u otros componentes de la placa madre. El calor del procesador se transfiere al disipador y luego el flujo de aire del gabinete de la computadora lo disipa. |
| Ventilador (*fan*) | Los ventiladores se pueden fijar al procesador, junto al procesador y en el gabinete. |
| Pasta térmica o almohadilla térmica | La pasta, el compuesto o la grasa térmica se puede aplicar sobre la parte superior de un procesador antes de fijar un disipador. Algunos disipadores y ventiladores tienen pasta térmica preaplicada. Una almohadilla térmica proporciona una dispersión uniforme del calor y se coloca entre el procesador y el disipador. |
| Enfriamiento líquido | El líquido circula por el sistema, incluido un disipador montado en la CPU. El calor del procesador se transfiere al líquido refrigerante. El líquido ya caliente se transporta a la parte trasera del sistema, se convierte en calor y se libera fuera del gabinete. La temperatura de la CPU permanece constante, independientemente del uso. Algunos sistemas requieren que el líquido se rellene periódicamente. |
| Enfriamiento por cambio de fase (enfriamiento por vapor) | Esta costosa opción usa una técnica similar a la de un refrigerador: un gas se convierte en líquido que se vuelve a convertir en gas. |

> Figura 3.18 Disipador de calor y ventilador

El chip más grande de la placa madre con un ventilador o un disipador de calor conectado se reconoce fácilmente como el procesador. La Figura 3.19 muestra un Intel Core i7 que tiene un ventilador y un disipador de calor instalados. Observa los tubos de calor (*heat pipes*) que se usan como parte del disipador.

> Figura 3.19 CPU con disipador de calor y ventilador conectados

### Consejo técnico: enfriar la CPU

No apliques energía a una computadora hasta que la CPU y el disipador de calor, el ventilador y/o la unidad de enfriamiento estén instalados. Hacer funcionar la CPU sin instalar mecanismos de enfriamiento adecuados sobrecalentará la CPU y la destruirá o debilitará.

Otros componentes de la placa madre también pueden tener disipadores de calor conectados. Normalmente son el chipset y/o los chips controladores de E/S (entrada/salida). La Figura 3.20 muestra una placa madre con estos elementos de enfriamiento.

> Figura 3.20 Disipadores de calor de la placa madre

### Consejo técnico: cuando la pasta térmica actúa como pegamento

Con el tiempo, la pasta térmica puede actuar como pegamento, dificultando separar un procesador de un disipador de calor. Puedes usar un limpiador de pasta térmica, acetona o alcohol desnaturalizado para separar las dos partes. ¡No las fuerces para separarlas!

## Instalar un procesador

Los procesadores se venden con instrucciones de instalación. Además, los manuales de la placa madre (u otra documentación) incluyen los pasos para actualizar o instalar la CPU. Los siguientes son las partes y los pasos generales para instalar un procesador:

**Partes:** Procesador adecuado para la placa madre (consulta la documentación de la placa madre) y materiales antiestáticos.

1. Asegúrate de que la energía de la computadora esté apagada y la computadora esté desenchufada.
2. Coloca una pulsera antiestática alrededor de tu muñeca y conecta el otro extremo a una conexión a tierra o a una parte metálica sin pintura de la computadora. Como alternativa, usa un guante antiestático.
3. Empuja la palanca de retención hacia abajo y hacia afuera para liberar la placa de retención de la CPU. Mueve la palanca hacia atrás hasta que la placa de retención esté completamente abierta. No toques el zócalo de la CPU. Si hay una cubierta de plástico instalada en el zócalo de la CPU, retírala.
4. Retira el procesador del empaque, cuidando de sostenerlo por los bordes y sin tocar nunca la parte metálica inferior del procesador. Recuerda que una CPU solo encaja de una manera en el zócalo. Mira el procesador y el zócalo antes de insertar el chip para garantizar una alineación correcta. Un zócalo y una CPU normalmente tienen una marca triangular o un punto para indicar el **pin 1**, como se muestra en la Figura 3.21. El procesador también tiene muescas en cada lado que se alinean con el zócalo. Inserta la CPU en el zócalo alineándola con el zócalo y bajándola hasta que quede a ras con él, como se muestra en la Figura 3.22. (¡No la fuerces!)

> Figura 3.21 Pin 1 y muesca en un procesador

> Figura 3.22 Instalar una CPU

### Consejo técnico: manipular la CPU

Sostén siempre una CPU por los bordes para evitar doblar o tocar los pines de abajo. No toques una CPU hasta que estés listo para instalarla en el zócalo.

## Actualizar procesadores

Dos preguntas comunes que se hacen a los técnicos son: «¿Se puede actualizar una computadora a un procesador más potente o rápido?» y «¿Se debería actualizar una computadora a un procesador más potente o rápido?». Que una computadora se pueda o no actualizar a un procesador más potente o rápido depende de la capacidad de la placa madre. Cuando un cliente pregunta si se debería actualizar un procesador, el técnico debe preguntar: «¿Qué sistema operativo y aplicaciones usa?». Cuanto más nuevo sea el sistema operativo, más avanzado debe ser el procesador. Algunos juegos y aplicaciones que deben realizar cálculos, así como las aplicaciones orientadas a gráficos, requieren un procesador más rápido y avanzado. La documentación de la placa madre es muy importante al considerar una actualización de CPU. Lee esta documentación para determinar si la placa madre puede aceptar un procesador más rápido.

### Consejo técnico: actualizar una CPU

No actualices un procesador a menos que la documentación o el fabricante indiquen que la placa madre admite un procesador más nuevo o rápido.

La **gestión de limitación** (*throttle management*) es el proceso de controlar la velocidad de una CPU ralentizándola cuando no se está usando intensamente o cuando está caliente. Por lo general, esta función la controlan un ajuste del BIOS/UEFI del sistema y el Panel de control de Opciones de energía de Windows. Algunos usuarios pueden querer que el rendimiento sea máximo y por eso no usar la limitación de la CPU. Los usuarios de portátiles, en cambio, pueden querer conservar energía siempre que sea posible para prolongar el tiempo que la computadora se puede usar con batería. Usa el enlace Configuración de batería de Windows para controlar cómo afectan las aplicaciones al rendimiento de la batería.

Actualizar componentes distintos del procesador también puede aumentar la velocidad de una computadora. Instalar más memoria y/o almacenamiento de mayor capacidad y más rápido comúnmente mejora el rendimiento de una computadora más que instalar un procesador nuevo. Todos los dispositivos y componentes electrónicos deben trabajar juntos para transferir los 1s y 0s de manera eficiente.

## Overclocking (sobrefrecuencia) de procesadores

El **overclocking** implica cambiar la velocidad del bus del lado frontal y/o el multiplicador para aumentar la velocidad de la CPU y del sistema. El overclocking tiene algunos problemas:

- El procesador, la placa madre, la memoria y otros componentes pueden dañarse por el overclocking.
- Las aplicaciones pueden fallar, el sistema operativo puede no arrancar y/o el sistema puede colgarse (bloquearse) al hacer overclocking.
- Puedes anular la garantía de algunas CPU si haces overclocking.
- Cuando aumentas la velocidad de la CPU, el calor del procesador aumenta. El enfriamiento extra, usando ventiladores y disipadores de calor más grandes, es esencial.
- Los dispositivos de entrada/salida pueden no reaccionar bien al overclocking.
- Es posible que los chips de memoria deban actualizarse para poder seguir el ritmo del procesamiento más rápido.
- Necesitas saber cómo restablecer el BIOS/UEFI del sistema en caso de que la computadora no arranque correctamente después de hacer los cambios. Este proceso se cubre en el Capítulo 4.

### Consejo técnico: estar listo para enfriar

El principal problema del overclocking es un enfriamiento insuficiente. Asegúrate de comprar un disipador de calor más grande y/o ventiladores adicionales antes de comenzar el proceso de overclocking.

Muchos fabricantes de placas madre no permiten cambios en la configuración de la CPU, el multiplicador y el reloj. Los cambios en la placa madre suelen hacerse a través de la configuración del BIOS/UEFI. Sin embargo, los fabricantes de CPU pueden proporcionar herramientas de ajuste en forma de aplicaciones instaladas en la computadora para la configuración del overclocking. Ten en cuenta que el overclocking es una situación de ensayo y error. Hay sitios web dedicados a documentar placas madre específicas y CPU con overclocking.

## Instalar soluciones térmicas para la CPU

Una CPU puede venir con una solución térmica, como un disipador de calor y/o un ventilador. La solución térmica comúnmente viene con una pasta térmica preaplicada o una almohadilla térmica (*thermal pad*) adherida. Los disipadores de calor y los ventiladores se conectan al procesador usando diferentes métodos, como tornillos, compuesto térmico y clips. Los clips pueden implicar tornillos de retención, liberación de presión o una ranura de retención. El tipo de disipador de calor y/o ventilador instalado debe encajar con el procesador y el gabinete. Es posible que se deba instalar herraje adicional en la placa madre para poder conectar una solución térmica de CPU. La Figura 3.23 muestra un enfriador de CPU siendo instalado.

> Figura 3.23 Instalación del disipador de calor/ventilador de la CPU

### Consejo técnico: tomar una foto de la CPU

Antes de conectar un disipador de calor y/o un ventilador a una CPU, toma una foto de las marcas de la parte superior. Es posible que necesites usar estas marcas si alguna vez necesitas soporte técnico y requieres las especificaciones exactas. Los técnicos suelen tomar fotos para documentar el reemplazo de placas madre y el cableado.

Si se va a instalar una solución térmica, entonces se debe retirar la almohadilla térmica o la pasta térmica vieja y aplicar pasta térmica nueva. No rayes la superficie de un disipador de calor. Usa un raspador o herramienta de plástico para retirar una almohadilla térmica o pasta vieja. Se puede usar un limpiador de pasta térmica, acetona o alcohol desnaturalizado con un paño sin pelusa para eliminar la pasta residual.

Al instalar pasta térmica, aplica la cantidad prescrita en el centro del procesador. Extiende el compuesto de manera uniforme en una capa fina sobre la porción central de la CPU que entra en contacto con el disipador de calor. Cuando el disipador de calor se conecta al procesador, el compuesto térmico se extenderá (ojalá que no sobre los bordes). Sigue siempre las instrucciones de instalación del disipador de calor.

Es probable que un ventilador de CPU tenga un cable de 3 o 4 pines que se conecta a la placa madre. La placa madre podría tener un conector de 3 o 4 pines. Un ventilador de 3 pines se puede conectar a un conector de placa madre de 4 pines, y un cable de ventilador de 4 pines se puede conectar a un conector de placa madre de 3 pines, como se muestra en la Figura 3.24. Ten en cuenta que, cuando un cable de 3 pines se conecta a un conector de 4 pines, el ventilador siempre está encendido y no se puede controlar, como sí puede hacerlo un cable de 4 pines en un conector de 4 pines.

> Figura 3.24 Conectividad del ventilador de la CPU

## Solución de problemas del procesador

Los problemas del procesador pueden aparecer de diferentes maneras, como se ilustra en la Figura 3.25.

> Figura 3.25 Detectar problemas del procesador

Los siguientes consejos pueden ayudarte a resolver problemas de CPU:

- El problema número uno relacionado con problemas del procesador es el calor. Asegúrate de que todos los ventiladores funcionen. Escucha si hay un ruido de rechinado (*grinding noise*) que indique que algo está atascado en el ventilador, falta de aceite o un ventilador que está fallando. Agregar ventiladores cuesta muy poco en comparación con reemplazar un procesador y/o una placa madre. Asegúrate de que la computadora tenga circulación/enfriamiento adecuados. Aspira el polvo de la placa madre/CPU. Enfría más la habitación.
- Muchas pantallas del BIOS/UEFI muestran la temperatura de la CPU. (Esto se cubre con más detalle en el Capítulo 4.)
- Investiga cualquier código visual que se muestre en los LED de la placa madre o escucha los pitidos de audio cuando arranca la computadora. Consulta el sitio web del fabricante de la computadora o de la placa madre.

Los problemas del procesador son difíciles de diagnosticar, y a menudo es muy complicado determinar si un problema es de la CPU o de la placa madre. Si tienes energía en el sistema (es decir, la fuente de poder tiene salida de energía), el disco duro funciona (pruébalo en otra computadora) y el monitor funciona (pruébalo en otra computadora), entonces la placa madre y/o la CPU son los principales sospechosos.

## Ranuras de expansión

Si una computadora ha de ser útil, la CPU debe comunicarse con el mundo exterior, incluidos otros componentes de la placa madre y los adaptadores conectados a la placa madre. Una **ranura de expansión** se usa para agregar un adaptador a la placa madre. La Figura 3.26 muestra ranuras de expansión en una placa madre.

> Figura 3.26 Ranuras de expansión de la placa madre

Un técnico debe poder distinguir entre adaptadores y ranuras de expansión, y debe poder identificar los adaptadores/dispositivos que usan ranuras de expansión. Un técnico también debe reconocer las capacidades y limitaciones de cada tipo de ranura de expansión al instalar actualizaciones, reemplazar piezas y hacer recomendaciones. Empecemos con el tipo más antiguo y avancemos.

### PCI (Peripheral Component Interconnect)

Una ranura de expansión anteriormente popular es **Peripheral Component Interconnect (PCI)**. También hubo una actualización del bus PCI llamada PCI-X que se encontraba comúnmente en servidores y no se cubre aquí, salvo con fines de comparación. La Figura 3.27 muestra el tipo más común de ranura de expansión PCI.

> Figura 3.27 Ranura de expansión PCI

### AGP (Accelerated Graphics Port)

**AGP (Accelerated Graphics Port)** es una interfaz de bus para adaptadores gráficos desarrollada a partir del bus PCI. Intel aportó la mayor parte del desarrollo de AGP. Con AGP, el subsistema de video queda aislado del resto de la computadora. La Figura 3.28 muestra una ilustración de una ranura AGP comparada con ranuras de expansión PCI. Ambos tipos de ranura de expansión han sido reemplazados por PCIe (que se cubre a continuación), pero como técnico todavía verás ambos.

> Figura 3.28 Ranuras de expansión AGP y PCI

### PCIe (Peripheral Component Interconnect Express)

PCI y AGP han sido reemplazados por **PCIe (PCI Express)**, que a veces también se escribe PCI-E. PCIe supera a todos los demás tipos de ranuras de expansión PCI. La Figura 3.29 muestra ranuras de expansión PCI, y la Tabla 3.6 enumera las distintas versiones de PCIe.

> Figura 3.29 Ranuras de expansión PCIe

> Tabla 3.6 Versiones de PCIe

| Versión de PCIe | Velocidad (por carril y por dirección) |
|---|---|
| 1.0 | 2.5 GT/s (gigatransferencias por segundo) o 250 MB/s |
| 2.0 | 5 GT/s o 500 MB/s |
| 3.0 | 8 GT/s o 1 GB/s |
| 4.0 | 16 GT/s o 2 GB/s |
| 5.0 | 32 GT/s o 4 GB/s |
| 6.0 | 64 GT/s o 8 GB/s |

El estándar PCI más antiguo es **bidireccional semidúplex** (*half-duplex*), lo que significa que los datos se envían hacia y desde la tarjeta PCI usando solo una dirección a la vez. PCIe envía datos de forma **bidireccional dúplex completo** (*full-duplex*); en otras palabras, puede enviar y recibir al mismo tiempo. La Figura 3.30 muestra este concepto.

### Consejo técnico: tarjetas PCI en ranuras PCIe

Los adaptadores PCI y AGP más antiguos no funcionarán en ningún tipo de ranura PCIe.

> Figura 3.30 Una comparación de las transferencias PCI y PCIe

Otra diferencia entre PCI y PCIe es que las ranuras PCIe vienen en distintas versiones, según el número máximo de carriles (*lanes*) que se pueden asignar a la tarjeta insertada en la ranura. Por ejemplo, una ranura x1 puede tener solo un carril de transferencia usado por la tarjeta x1 insertada en la ranura; también hay ranuras x2, x4, x8 y x16. El estándar admite una ranura x32, pero estas ranuras son raras debido a su longitud. Una ranura x16 acepta hasta 16 carriles, pero se pueden asignar menos carriles. La Figura 3.31 muestra el concepto de carriles PCIe. Observa que un carril tiene dos canales de comunicación unidireccionales. También observa que solo se usan siete carriles. PCIe tiene la capacidad de usar un número reducido de carriles si un carril experimenta una falla o un problema de rendimiento.

> Figura 3.31 Carriles PCIe

### Consejo técnico: cuidado con la letra pequeña de PCIe

Algunos fabricantes de placas madre ofrecen un tamaño de ranura más grande (como x8), pero la ranura funciona a una velocidad más lenta (x4, por ejemplo). Esto mantiene bajo el costo. El manual mostraría tal ranura como x8 (modo x4) en la descripción de la ranura PCIe.

Un adaptador PCIe x1 puede caber en una ranura x1 o superior. Una tarjeta más grande, como una PCIe x16, no puede caber en una ranura de número menor (x8, x4, x2 o x1). La Figura 3.32 muestra este concepto.

> Figura 3.32 Ranuras correctas para tarjetas PCIe

Quitar un adaptador normalmente es solo cuestión de quitar un tornillo de retención o levantar una placa de retención y levantar el adaptador fuera de la ranura. Algunas ranuras de expansión tienen palancas de retención. Mueves la palanca de retención hacia un lado para levantar el adaptador de la ranura de expansión. La Figura 3.33 muestra un ejemplo del proceso de extracción de un adaptador PCIe. La Figura 3.34 muestra una placa madre con dos PCIe x1, dos PCIe x16 y tres ranuras de expansión PCI. Observa que las ranuras PCIe x16 tienen una palanca de retención.

### Consejo técnico: extraer adaptadores PCIe

Los adaptadores PCIe x16 comúnmente tienen palancas de liberación. Debes presionar la palanca mientras extraes el adaptador de la ranura de expansión, o podrías dañar la placa (y posiblemente la placa madre).

> Figura 3.33 Extracción de un adaptador PCIe

> Figura 3.34 Placa madre con ranuras PCIe y PCI

## Opciones de seguridad de la placa madre

Las placas madre pueden contener opciones de seguridad que ayudan a proporcionar más seguridad para las aplicaciones y los datos. Una placa madre puede contener un **módulo de plataforma segura (TPM)** o una ranura para instalar uno. Un TPM se puede usar para proteger datos, almacenar certificados de seguridad digitales, almacenar contraseñas o verificar la integridad de los archivos del sistema operativo. Microsoft Windows 11 requiere que se instale un TPM antes de que el sistema operativo funcione. El TPM se habilita y configura a través del BIOS/UEFI, que se cubre en el Capítulo 4. La Figura 3.35 muestra un TPM.

> Figura 3.35 TPM

Otra opción de seguridad similar es un **módulo de seguridad de hardware (HSM)**, que se puede instalar como adaptador para realizar algunas de las mismas funciones que un TPM. Un HSM tiene un criptoprocesador u otros chips que se usan para crear, gestionar y almacenar claves de seguridad y se usan en el cifrado de datos y dispositivos de almacenamiento.

## Tipos de placas madre

Las placas madre vienen en diferentes tamaños, conocidos como **factores de forma** (*form factors*). El factor de forma de placa madre de escritorio más común es **Advanced Technology Extended (ATX)**. Otros factores de forma ATX incluyen micro-ATX (a veces escrito μATX o mATX), mini-ATX, FlexATX, EATX, WATX, nano-ATX, pico-ATX y mobileATX.

Un factor de forma de placa madre más grande y con mejor flujo de aire (pero que no es tan popular como ATX y micro-ATX) es **Balanced Technology eXtended (BTX)**. Un factor de forma más pequeño es **Information Technology eXtended (ITX)**, que viene en tamaños mini-ITX, nano-ITX y pico-ITX. La Figura 3.36 muestra algunos de los factores de forma de placa madre, y la Tabla 3.7 proporciona información consolidada sobre los principales factores de forma. La Figura 3.37 muestra una placa madre más antigua con muchos de los componentes de la placa madre etiquetados.

> Figura 3.36 Factores de forma de placas madre

> Tabla 3.7 Comparación de factores de forma de placas madre

| Factor de forma | Descripción | Tamaño |
|---|---|---|
| BTX | Se usa en computadoras de escritorio | 12.8 × 10.5 pulgadas (32.5 × 26.7 cm) |
| ATX | Se usa en computadoras de escritorio | 12 × 9.6 pulgadas (30.5 × 24.4 cm) |
| mATX | MicroATX: una placa madre de escritorio más pequeña | 9.6 × 9.6 pulgadas (24.4 × 24.4 cm) |
| ITX o mITX | Se usa en computadoras muy pequeñas y decodificadores (*set-top boxes*) | 6.7 × 6.7 pulgadas (17 × 17 cm) |

### Consejo técnico: hacer coincidir el factor de forma de la placa madre y el gabinete

El gabinete usado para una computadora debe coincidir con el factor de forma de la placa madre. Algunos gabinetes pueden alojar diferentes factores de forma, pero siempre debes verificarlo. Cuando armas una computadora o reemplazas una placa madre, es importante obtener el factor de forma correcto.

> Figura 3.37 Componentes de una placa madre de estación de trabajo ASUS

Los fabricantes a veces diseñan un gabinete de modo que requiera una placa madre propietaria. Con tal diseño, se debe comprar una placa madre de reemplazo al fabricante original y, por lo general, es más cara que una opción genérica.

## Actualizar y reemplazar placas madre

La siguiente lista te guía para tomar la decisión (o ayudar a un cliente a tomarla) sobre si actualizar una placa madre:

- ¿Por qué se está actualizando la computadora? A veces actualizar la placa madre no ayuda a menos que se actualicen los demás componentes de la computadora. Si el acceso al software es lento, la solución podría no ser una placa madre nueva, sino un disco duro más rápido y de mayor capacidad, una SSD nueva/de alta capacidad o más RAM.
- ¿Qué tipo de ranura de expansión (PCI, AGP o PCIe) y cuántos adaptadores de cada tipo se necesitan de la placa madre antigua? ¿La placa madre nueva tiene las ranuras de expansión requeridas?
- ¿Es compatible la placa madre? Verifica qué fabricante y modelos de CPU son compatibles. ¿La placa madre nueva cabrá en el gabinete actual, o se requiere uno nuevo?
- Si se actualiza la CPU, ¿la placa madre admitirá la nueva CPU?
- ¿Funcionarán los chips de memoria antiguos en la placa madre nueva o con la CPU nueva?

### Consejo técnico: placas madre en otros tipos de dispositivos

Ten en cuenta que las placas madre de servidor, las placas madre de portátil y las placas madre de otros dispositivos móviles tienden a ser propietarias, y tienes que comprar un reemplazo al fabricante.

Antes de reemplazar una placa madre, es importante hacer todo lo siguiente:

- Quitar la CPU y el ventilador de la CPU.
- Quitar los adaptadores de las ranuras de expansión.
- Quitar los chips de memoria de las ranuras de expansión.
- Desconectar los conectores de energía.
- Desconectar los cables planos (*ribbon cables*).
- Desconectar los dispositivos externos como ratón, teclado y monitor.

Las placas madre de reemplazo normalmente no vienen con RAM, así que los módulos antiguos se retiran de la placa madre averiada/más antigua. Una placa madre por lo general no viene con CPU. Al actualizar cualquier componente o una computadora entera, recuerda que la pieza más antigua se puede donar a una organización benéfica o a una institución educativa.

### Consejo técnico: usar buenas medidas antiestáticas al instalar una placa madre

Al reemplazar una placa madre, coloca la placa madre sobre una superficie no conductora, como una alfombrilla antiestática o la bolsa antiestática que vino con la placa madre.

## Solución de problemas de la placa madre

Los síntomas comunes de problemas de la placa madre son similares a los síntomas de problemas de la CPU: el sistema tiene una **pantalla en blanco o pantalla negra** al arrancar (lo que podría significar que el cable de video no está bien conectado o que el sistema no tiene energía/no está encendido); aparece un código de error; ocurren uno o más pitidos; el sistema experimenta un **apagado inesperado**, un **apagado intermitente** o un **bloqueo del sistema**; el sistema puede reiniciarse continuamente; aparece una **BSOD de Windows (pantalla azul de la muerte)**; o falla uno o más de los puertos, ranuras de expansión o módulos de memoria. Ten en cuenta que los apagados inesperados/intermitentes, los bloqueos del sistema y los reinicios continuos también pueden ser síntomas de un problema de CPU o de fuente de poder.

Los problemas de placa madre y los problemas de energía son probablemente los más difíciles de diagnosticar. Debido a que varios componentes se encuentran en la placa madre, muchas cosas pueden causar errores. El **POST** (*power-on self-test*) es una de las ayudas más beneficiosas para diagnosticar una placa madre y puede incluir una serie de **pitidos del POST** (*POST beeps*). Se debe investigar el significado de cualquier código que aparezca en la pantalla. Si aparecen múltiples códigos de error de POST, debes diagnosticarlos en el orden en que se presentan. El Capítulo 11, «Revisión de diseño y solución de problemas de computadoras», describe los pitidos y errores comunes, pero ten en cuenta que los fabricantes pueden tener sus propias **pantallas propietarias de fallos** y errores.

La siguiente lista ayuda con la solución de problemas de la placa madre:

- ¿La placa madre recibe energía? Verifica la fuente de poder para ver si el ventilador gira. Si la CPU o la placa madre tiene un ventilador, mira si gira. Verifica los voltajes que van de la fuente de poder a la placa madre. Consulta el Capítulo 5, «Desarmado y energía», para obtener indicaciones.
- Verifica la exactitud de la configuración del BIOS/UEFI (se cubre en el Capítulo 4).
- Verifica si hay sobrecalentamiento, lo que podría indicar un problema con la CPU o la placa madre. ¿La placa madre está caliente al tacto o emite olor a quemado? Apaga la computadora y deja que se enfríe. Enciende la computadora con la cubierta retirada. Mira si el ventilador de la CPU gira.
- Verifica si hay **hinchazón de capacitores** en la placa madre: pequeños componentes que pueden parecer abultados. Si miras de nuevo la Figura 3.34, puedes ver los cilindros metálicos (que son capacitores) en la esquina inferior derecha y junto a las ranuras de expansión. Si ves que tal capacitor está hinchado, reemplaza la placa madre lo antes posible.
- Vuelve a asentar (*reseat*) la CPU, los adaptadores y los chips de memoria.
- Quita los adaptadores y dispositivos innecesarios y arranca la computadora.
- Enchufa la computadora a un tomacorriente y circuito diferentes, si es posible.
- Verifica si la placa madre está haciendo cortocircuito con el chasis.
- Verifica la batería del CMOS. (Consulta el Capítulo 5 para saber cómo tomar lecturas de voltaje.)
- Con una placa madre que tiene LED de diagnóstico, verifica la salida para cualquier código de error. Consulta la documentación de la placa madre o la documentación en línea para conocer el problema y la posible solución.

### Consejo técnico: estos conceptos también se relacionan con las computadoras Apple

Aunque este libro se centra en las PC, los conceptos relacionados con las CPU, las placas madre, las ranuras de expansión, la caché y los chipsets también se aplican a las computadoras Apple. Las computadoras Apple y las PC tienen requisitos de CPU y memoria similares.

## Habilidades blandas: la escucha activa

La escucha activa es participar en una conversación en la que te concentras en lo que dice el cliente; es decir, escuchar más que hablar. Para un técnico, la escucha activa tiene los siguientes beneficios:

- Te permite reunir datos y síntomas rápidamente
- Te permite establecer una buena relación (*rapport*) con el cliente
- Mejora tu comprensión del problema
- Te permite resolver el problema más rápido porque comprendes mejor el problema
- Proporciona entendimiento mutuo entre tú y el cliente
- Proporciona un medio para tener una conversación positiva y comprometida en lugar de un encuentro negativo y confrontacional
- Se centra en el cliente en lugar del técnico
- Proporciona un entorno en el que el cliente podría ser más comunicativo con información relacionada con el problema

Con frecuencia, cuando un técnico llega al sitio o contacta a un cliente que tiene un problema técnico, el técnico va con prisa; pensando en otras cosas, incluidos los problemas que hay que resolver; asumiendo que sabe exactamente cuál es el problema, aunque el usuario no haya terminado de explicarlo; o más interesado en el problema técnico que en el cliente y sus dificultades. La escucha activa cambia el foco de los problemas del técnico a los problemas del cliente.

Una llamada de servicio común pero ineficaz implica que el técnico hable y pregunte la mayor parte del tiempo, usando jerga y acrónimos técnicos y un tono plano o condescendiente. Un cliente que se siente vulnerable experimenta un mayor nivel de ansiedad. La escucha activa cambia este escenario ayudándote a construir una relación profesional con tus clientes. La Figura 3.38 muestra a un técnico escuchando activamente. La siguiente lista describe algunas medidas que te ayudan a implementar la escucha activa.

> Figura 3.38 Escucha activa

Mantén una actitud profesional positiva y comprometida al hablar y escuchar a los clientes:

- Deja atrás tus prejuicios; sé educado y consciente de otras culturas y costumbres; sé de mente abierta y sin prejuicios.
- Ten una actitud cálida y atenta.
- No cruces los brazos frente al pecho, porque hacerlo te distancia del problema y del cliente.
- No culpes a otros ni hables mal de otros técnicos.
- No actúes como si el problema no fuera tu responsabilidad.

Concéntrate en lo que dice el cliente:

- Apaga o ignora tus dispositivos electrónicos.
- Mantén el contacto visual; no dejes que tu mente divague.
- Permite que el cliente termine de explicar el problema; no interrumpas; evita discutir con el cliente o ponerte a la defensiva.
- Detén todos los comportamientos y actividades irrelevantes.
- Revisa mentalmente lo que dice el cliente.
- Abstente de hablar innecesariamente con compañeros de trabajo mientras interactúas con los clientes.
- Evita interrupciones o distracciones personales.

Participa en la conversación de manera limitada pero activa:

- Mantén una conducta profesional (suspende las emociones negativas); no minimices ni menosprecies el problema del cliente.
- Reconoce que estás escuchando asintiendo de vez en cuando y haciendo comentarios como «Ya veo».
- Usa lenguaje corporal positivo, como inclinarte ligeramente hacia adelante o tomar notas.
- Observa el comportamiento del cliente para determinar cuándo es apropiado hacer preguntas.

Habla brevemente con el cliente:

- Habla con un tono positivo; usa un tono empático y genuino, no condescendiente.
- Reformula o resume los puntos expresados por el cliente.
- Haz preguntas no amenazantes y de sondeo relacionadas con las declaraciones o preguntas del cliente.
- No saltes entre temas.
- No uses jerga técnica.
- Aclara el significado de la situación del cliente.
- Identifica pistas para ayudar a resolver el problema y reducir tu tiempo de diagnóstico escuchando con atención lo que dice el cliente.
- Haz seguimiento con la persona más adelante para asegurarte de que el problema esté resuelto y verificar la satisfacción.
- Ofrece diferentes opciones de reparación o reemplazo, si es posible.

## Resumen del capítulo

- Las partes importantes de la placa madre incluyen: CPU, ranuras de RAM, RAM, ranuras de expansión (PCI, PCIe y AGP) y dispositivos de enfriamiento.
- Los procesadores ARM son populares en dispositivos móviles (pero se pueden usar en computadoras de escritorio y servidores), consumen menos energía, producen menos calor y cuestan menos que los procesadores Intel o AMD. Los procesadores de escritorio pueden ser multinúcleo y pueden contener memoria caché muy rápida: L1, L2 y L3.
- Los procesadores Intel usan Hyperthreading para hacer un uso eficiente del tiempo del procesador mientras la CPU ejecuta conjuntos separados de instrucciones simultáneamente.
- Los procesadores deben mantenerse fríos con ventiladores y/o disipadores de calor. Se aplica una pasta o almohadilla térmica entre un disipador de calor y un procesador. Nunca enciendas una computadora sin algún tipo de enfriamiento instalado.
- La velocidad de reloj se refiere al reloj interno del procesador. No es lo mismo que el FSB o la velocidad del bus.
- La limitación de CPU (*throttling*) ralentiza el procesador para evitar el sobrecalentamiento.
- PCI es un bus paralelo de 32 y 64 bits. PCI y AGP han sido reemplazados por el bus serie PCIe.
- Las ranuras PCIe tienen un número específico de carriles bidireccionales que es el máximo que una tarjeta puede usar. Un adaptador PCIe puede caber en una ranura del mismo número de carriles o en una ranura que tenga la capacidad de procesar un número mayor de carriles.
- Una GPU integrada está en el mismo dado que la CPU y procesa funciones relacionadas con los gráficos.
- Al reemplazar una placa madre, asegúrate de que el factor de forma, el zócalo de CPU y el número/tipos de ranuras de expansión sean apropiados.
- Un TPM o HSM aumenta la seguridad almacenando certificados de seguridad digitales y contraseñas y protegiendo los datos.
- Usa el POST para diagnosticar problemas de placa madre o CPU. Los síntomas de problemas de CPU o placa madre incluyen capacitores hinchados, apagados inesperados/intermitentes, bloqueos del sistema, pantalla en blanco al arrancar, reinicios continuos y sobrecalentamiento.
- La escucha activa es una habilidad importante para un técnico. Evita distraerte con personas o tecnología y toma notas, mantén buen contacto visual y haz preguntas dirigidas cuando sea apropiado.

### Consejos para el examen de certificación A+

- Conoce los siguientes tipos de conectores de placa madre: PCI, PCIe, eSATA, tipos de zócalo (incluido el término multizócalo) y *headers*. Ten en cuenta que las placas madre de servidor y móviles con frecuencia son elementos propietarios.
- Conoce las siguientes características de la arquitectura de CPU: x64/x86, ARM, un solo núcleo, multinúcleo, multithreading y soporte de virtualización.
- Repasa los diagramas de las ranuras de expansión PCI y PCIe. Usa internet para ver placas madre y comprobar si puedes determinar el tipo de ranura de expansión. Haz lo mismo con otros componentes de la placa madre, incluido el procesador. Prepárate para etiquetar gráficos en el examen.
- Conoce que Intel y AMD son dos fabricantes de CPU prominentes que requieren una placa madre y un zócalo adecuados para instalar el procesador.
- Repasa los tipos de métodos de enfriamiento de CPU: ventilador, disipador de calor, líquido y pasta/almohadillas térmicas.
- Sé capaz de instalar una CPU y un sistema de enfriamiento. Conoce cómo y dónde conectar un ventilador de CPU.
- Conoce las diferencias entre los factores de forma de placa madre ATX, ITX y BTX, y sé capaz de identificarlos.
- Conoce las diferencias entre un TPM y un HSM.
- Conoce los síntomas de problemas del procesador y de la placa madre: capacitor hinchado, apagados inesperados/intermitentes, bloqueos del sistema, pantalla en blanco o negra al arrancar, reinicios continuos, sobrecalentamiento y olor a quemado. Usa los códigos POST para ayudar con la solución de problemas.

## Términos clave

- Escucha activa — *active listening*
- AGP
- AMD
- APU
- Procesador ARM — *ARM processor*
- ATX
- Pantalla negra — *black screen*
- Pantalla en blanco — *blank screen*
- Pantalla azul de la muerte — *blue screen of death*
- Olor a quemado — *burning smell*
- Memoria caché — *cache memory*
- Hinchazón de capacitores — *capacitor swelling*
- Reloj — *clock*
- Velocidad de reloj — *clock speed*
- Reinicio continuo — *continuous reboot*
- CPU
- Zócalo de CPU — *CPU socket*
- Velocidad de CPU — *CPU speed*
- Limitación de CPU — *CPU throttling*
- Bus de datos externo — *external data bus*
- Ventilador — *fan*
- Factor de forma — *form factor*
- FSB
- GPU
- Ruido de rechinado — *grinding noise*
- Disipador de calor — *heat sink*
- HSM
- Hyperthreading
- HyperTransport
- GPU integrada — *integrated GPU*
- Intel
- Apagado intermitente — *intermittent shutdown*
- Bus de datos interno — *internal data bus*
- ITX
- Caché L1 — *L1 cache*
- Caché L2 — *L2 cache*
- Caché L3 — *L3 cache*
- Enfriamiento líquido — *liquid cooling*
- micro-ATX
- Placa madre de dispositivo móvil — *mobile device motherboard*
- Multinúcleo — *multicore*
- Multizócalo — *multisocket*
- Multithreading
- Overclocking
- Sobrecalentamiento — *overheating*
- PCI
- PCIe
- POST
- Pitidos del POST — *POST beeps*
- Procesador — *processor*
- Pantalla propietaria de fallos — *proprietary crash screen*
- Placa madre de servidor — *server motherboard*
- Procesador de un solo núcleo — *single-core processor*
- Bloqueo del sistema — *system lockup*
- Almohadilla térmica — *thermal pad*
- Pasta térmica — *thermal paste*
- Hilo — *thread*
- Gestión de limitación — *throttle management*
- TPM
- Apagado inesperado — *unexpected shutdown*
- Virtualización — *virtualization*
- Soporte de virtualización — *virtualization support*
- VM
- x64
- x86
- Zócalo ZIF — *ZIF socket*

## Preguntas de repaso

1. ¿Qué componente puede estar tanto en una tarjeta de video como en una placa madre?
   [ TPM | ranura de expansión PCIe | ranura de expansión PCI | GPU ]

2. ¿Qué ranura de expansión es mejor para una tarjeta de video en una computadora de escritorio nueva?
   [ PCIe | PCI | USB | AGP ]

3. Una placa madre tiene una ranura de expansión PCIe x16. ¿Qué adaptador(es) PCIe cabrán en esta ranura? (Elige todos los que correspondan.)
   [ x1 | x2 | x4 | x8 | x16 | x32 ]

4. Empareja la parte de la placa madre con la descripción correspondiente.
   - ____ caché L1 — a. Montada encima de la CPU
   - ____ CPU — b. Memoria que se encuentra en la CPU
   - ____ FSB — c. Ejecuta instrucciones de software
   - ____ disipador de calor — d. Bus entre la CPU y los componentes de la placa madre
   - ____ HT — e. Ralentiza la CPU para enfriarla
   - ____ limitación (*throttling*) — f. Permite que un procesador maneje múltiples instrucciones simultáneamente

5. ¿Qué es el bus del lado frontal?
   a. El bus de datos interno que conecta el núcleo del procesador con la caché L1
   b. El bus de datos interno que conecta el núcleo del procesador con la caché L2
   c. El bus de datos externo que conecta el procesador con los componentes de la placa madre
   d. El bus de datos externo que conecta el procesador con la caché L2

6. Un cliente quiere actualizar la caché L2. ¿Cuál de los siguientes requiere esto definitivamente?
   a. Comprar una placa madre
   b. Comprar una CPU
   c. Comprar una tarjeta de video
   d. Comprar un módulo de RAM

7. Empareja la ranura de expansión con su definición.
   - ____ AGP — a. Bus paralelo de 32 o 64 bits
   - ____ PCI — b. Solo para tarjetas de video
   - ____ PCIe — c. Tiene un número variable de carriles

8. ¿Cuál es la diferencia entre Hyperthreading y HyperTransport?

9. ¿Qué debe hacer un técnico si encuentra un capacitor hinchado en una placa madre?
   a. Reemplazar el capacitor.
   b. Reemplazar la placa madre.
   c. Verificar los voltajes que provienen de la fuente de poder.
   d. Reemplazar la fuente de poder.

10. ¿Cuál de las siguientes afirmaciones es verdadera respecto a PCIe?
    a. Una ranura PCIe no aceptará una tarjeta PCI.
    b. PCIe es una tecnología de bus paralelo.
    c. PCIe es una tecnología de bus de 32 o 64 bits.
    d. PCIe está siendo reemplazado por PCI-X.

11. [ V | F ] Un adaptador PCIe x8 siempre transmite usando ocho carriles.

12. ¿Cuál es el significado de una especificación de placa madre que indica lo siguiente: ranura 1 PCIe x16 (modo x8)?
    a. La ranura acepta tarjetas x8 o x16.
    b. La ranura puede transmitir tráfico usando 8 o 16 carriles.
    c. La ranura puede transmitir en ráfagas de 8 o 16 bytes a la vez.
    d. La ranura acepta tarjetas x16 pero usa solo 8 carriles.

13. ¿Cuáles son dos opciones de seguridad que ayudarían con la gestión de contraseñas y el cifrado? (Elige dos.)
    [ CPU | TPM | estándar PCIe | GPU | HSM ]

14. Un técnico de una universidad va a reparar un problema en otro edificio. Una profesora detiene al técnico para hablar sobre su computadora lenta. El técnico pone un poco los ojos en blanco pero luego se detiene y escucha a la profesora. La profesora comenta: «No puedo acceder a mi correo ni siquiera escribir mis exámenes. La computadora tarda al menos 20 minutos solo en arrancar». El técnico mira a su alrededor, un poco exasperado, y dice: «Ajá». «Registré este problema hace más de una semana», continúa la profesora, «y nadie ha pasado». «Ajá», responde el técnico de nuevo. «¿Sabes cuándo podrían encargarse de ese problema o tienes alguna idea de cuál podría ser el problema?», pregunta la profesora. El técnico mira a la profesora y dice: «Probablemente sea un virus que ha estado circulando. Se supone que Jim se encargaría de esos. Te atenderemos lo antes posible». Suena el teléfono del técnico y se aleja para atender la llamada.
    Enumera tres técnicas de escucha activa y buenos procedimientos de atención al cliente que podrían mejorar esta situación.

15. Explica cómo un técnico podría ser culturalmente insensible.

16. ¿Qué componente se puede ajustar para hacer overclocking?
    [ disipador de calor | CPU | ranura de expansión | chipset ]

17. [ V | F ] Al instalar una CPU, orienta el pin 1 con el pin 1 del zócalo y alinea los demás pines. Baja la palanca del zócalo ZIF y bloquea. Enciende la computadora para asegurarte de que la CPU funcione. Apaga la computadora e instala el disipador de calor y/o el ventilador.

18. ¿Qué se aplica entre un procesador y un disipador de calor para aumentar la disipación de calor?
    [ un capacitor | pasta térmica | un ventilador | memoria caché ]

19. Al revisar las especificaciones de la placa madre, ves LGA 2066. ¿Qué componente se está mencionando?
    [ RAM | HSM | procesador | ranura de expansión ]

20. ¿Qué método NO se usa para enfriar un procesador?
    [ ventilador de CPU | ventilador del gabinete | disipador de calor | tanque térmico ]

## Ejercicios

### Ejercicio 3.1 Identificar las partes de una placa madre ATX

**Objetivo:** Identificar varias partes de la placa madre.

**Materiales:** Ninguno.

**Procedimiento:** Identifica cada una de las partes de la placa madre ATX en la Figura 3.39.

> Figura 3.39 Puertos, ranuras y partes de la placa madre

1. PS/2 o mini-DIN
2. DVI o DVI-I
3. USB
4. NIC, puerto de red, RJ45 o puerto Ethernet
5. PCIe x1
6. PCIe x16
7. PCI
8. Ranura de expansión de memoria
9. Zócalo de CPU o de procesador

### Ejercicio 3.2 Análisis de la placa madre

**Objetivo:** Identificar varias partes de la placa madre.

**Materiales:** Ninguno.

**Procedimiento:** Usando la información que aprendiste en este capítulo y relacionada con las especificaciones que se encuentran en la Figura 3.40, responde las preguntas que siguen.

> Figura 3.40 Anuncio de una placa madre de escritorio

1. Si compraras esta placa madre, ¿qué tipo de gabinete necesitarías comprar?
2. ¿Qué te dice LGA1155 sobre esta placa madre?
3. ¿Esta placa madre viene con una CPU instalada?
   [ Sí | No | No se puede saber con la información presentada ]
4. ¿Qué componente de la placa madre controla el número máximo de puertos USB 3.0 que podría tener esta placa madre?
   [ CPU | RAM | chipset | FSB ]
5. ¿Qué procesador(es) acepta esta placa madre?
6. ¿Qué crees que significan las letras O.C. después de algunos de los chips de memoria en relación con esta placa madre?
7. ¿Cuál es la diferencia más significativa entre una ranura PCIe versión 2.0 y una ranura de expansión PCIe versión 3.0?
8. ¿Qué significa la línea PCIe 3.0/2.0 x16 que dice «2 (x16 único o x8 doble)»?
   a. El adaptador que va en esta ranura puede usar un solo carril que va a velocidades x16 o dos carriles que van a velocidades x8.
   b. Un solo adaptador x16 y/o un solo adaptador x8 pueden ir en las ranuras de expansión.
   c. Un adaptador x16 puede ir en una de las ranuras versión 3.0 y alcanzar velocidades 3.0, o se pueden instalar dos adaptadores x16, pero solo pueden transferir ocho carriles a la vez a velocidades 3.0.
   d. Un solo adaptador x16 se puede instalar en una de las ranuras versión 3.0, o se pueden instalar dos adaptadores x8 en las dos ranuras versión 3.0.
9. ¿Qué cable de dispositivo se puede insertar en el puerto PS/2? (Elige la mejor respuesta.)
   [ parlante | ratón o teclado | pantalla | almacenamiento externo ]
10. ¿Qué tipo de puerto de video se describe como D-sub en esta documentación?
    [ DisplayPort | DVI | HDMI | VGA ]
11. ¿Cuál es una ventaja de tener una GPU integrada en la CPU?
12. ¿Cuál es la razón más probable por la que este fabricante de placa madre eligió incluir dos ranuras de expansión PCI?
13. ¿Cuántos tipos diferentes de puertos de video tiene esta placa madre? Enuméralos.
14. ¿Cuál es el propósito del puerto S/PDIF out?
    [ video | audio | red inalámbrica | conectividad de dispositivos de entrada ]
15. ¿Es esta placa madre una placa madre multizócalo? ¿Cómo puedes saberlo?
    [ Sí | No ] Solo se enumera un zócalo, y esta es una placa madre de escritorio. Las placas madre de servidor tienen múltiples zócalos para las CPU.

## Actividades

### Descubrimiento en internet

**Objetivo:** Obtener información específica de internet sobre una computadora o sus partes asociadas.

**Materiales:** Una computadora con acceso a internet.

**Procedimiento:** Localiza en internet la documentación de una placa madre ASUS Prime Z590-A para responder las Preguntas 1 a 12. Continúa tu búsqueda en internet para responder las Preguntas 13 y 14.

**Preguntas:**

1. ¿La placa madre admite un procesador Intel o AMD?
2. ¿Qué chipset se usa?
3. ¿Cuántas ranuras de expansión hay en la placa madre?
4. ¿Qué factor de forma usa esta placa madre?
5. ¿Qué procesadores se pueden usar en esta placa madre?
6. ¿La placa madre admite tener una GPU integrada en la CPU? ¿Cómo puedes saber si lo admite o no?
7. ¿Qué tipo de zócalo de CPU tiene la placa madre?
8. ¿Cuántas ranuras PCIe tiene y de qué tipo?
9. ¿Hay algún otro tipo de ranura en esta placa madre? Si es así, ¿cuál?
10. ¿Esta placa madre tiene un puerto USB 3.2 integrado?
11. ¿Cuál es el número máximo y el tipo de puertos USB disponibles en la parte trasera de la placa madre?
12. Escribe la URL donde encontraste la información de la placa madre.
13. Encuentra un vendedor de una placa madre AMD que use el zócalo AM4 y admita los procesadores de escritorio Ryzen 2000, 3000 y 5000. Documenta el modelo de placa madre y el vendedor.
14. Encuentra un sitio de internet que describa las dimensiones del factor de forma de placa madre ATX extendido. Enumera las dimensiones y el sitio web.

### Habilidades blandas

**Objetivo:** Mejorar y afinar la capacidad de un futuro técnico para escuchar, comunicarse de forma escrita y oral, y apoyar de manera profesional a las personas que usan computadoras.

**Actividades:**

1. En una hoja de papel o una tarjeta, enumera tres formas en que puedes practicar la escucha activa en la escuela. Comparte esta información con tu grupo. Consolida las ideas y presenta cinco de las mejores ideas a la clase.
2. En un entorno de equipo, propongan dos ejemplos de situaciones que hayan vivido en las que una persona de soporte (una persona de soporte de PC, un vendedor, un cajero, una persona a la que se le piden direcciones, etc.) podría haber brindado mejor servicio si hubiera estado escuchando activamente. Compartan sus hallazgos con la clase.
3. En equipos de dos, hagan que una persona cuente una historia y la otra practique habilidades de escucha activa. La persona que cuenta la historia debe criticar al oyente. Luego la pareja debe cambiar los roles.

### Habilidades de pensamiento crítico

**Objetivo:** Analizar y evaluar información y aplicar la información aprendida a situaciones nuevas o diferentes.

**Actividades:**

1. Encuentra un anuncio de una computadora en un folleto de computadoras local, un periódico, una revista o un libro, o en internet. Determina toda la información sobre la placa madre y los puertos que puedas a partir del anuncio. Anota cualquier información que no entiendas. Investiga esta información y comparte tus hallazgos con un compañero de clase.
2. Tus padres quieren regalarte una computadora nueva. La que están considerando tiene una GPU integrada en la CPU. Enumera al menos un argumento que podrías usar para conseguir un modelo de computadora diferente.
3. ¿Por qué crees que una placa madre tiene diferentes buses que operan a distintas velocidades?
