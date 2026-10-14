# Capítulo 6. Memoria

> Traducción al español del Capítulo 6 («Memory») de *Complete A+ Guide to IT Hardware and Software: CompTIA A+ Exams 220-1101 & 220-1102* (Cheryl A. Schmidt, Christopher Lee) — material de estudio de uso personal.
>
> Nota: las figuras del libro son imágenes y no se incluyen aquí; se conserva su leyenda traducida como referencia. Las tablas se transcriben como tablas de Markdown.

En este capítulo aprenderás:

- Las diferentes tecnologías de memoria
- Cómo planificar una instalación o actualización de memoria
- Cómo instalar y extraer módulos de memoria
- Cómo optimizar la memoria para las plataformas Windows
- Las mejores prácticas para solucionar problemas de memoria
- Los beneficios del trabajo en equipo

**Objetivos del examen CompTIA:**

- 1101-3.2 Dado un escenario, instalar la RAM adecuada.
- 1101-3.3 Dado un escenario, seleccionar e instalar dispositivos de almacenamiento.
- 1101-5.2 Dado un escenario, diagnosticar problemas relacionados con placas madre, RAM, CPU y energía.
- 1102-1.3 Dado un escenario, usar características y herramientas del sistema operativo (SO) Microsoft Windows 10.
- 1102-1.4 Dado un escenario, usar la utilidad adecuada del Panel de control de Microsoft Windows 10.
- 1102-4.7 Dado un escenario, usar técnicas de comunicación y profesionalismo adecuadas.

## Descripción general de la memoria

Los sistemas informáticos necesitan software para funcionar, y el software reside en la memoria de la computadora. Un técnico debe entender la terminología de la memoria, determinar la cantidad óptima de memoria para un sistema, instalar la memoria, ajustarla para obtener el mejor rendimiento y solucionar cualquier problema de memoria.

El principal tipo de memoria que se encuentra en la placa madre es la **memoria de acceso aleatorio (RAM)**, específicamente la **RAM dinámica (DRAM)**. El otro tipo de RAM es la **RAM estática (SRAM)**. La DRAM es menos costosa pero más lenta que la SRAM. Con la DRAM, los 1 y 0 dentro del chip deben refrescarse. Con el tiempo, la carga, que representa la información dentro de un chip DRAM, se filtra. La información, que se almacena en 1 y 0, se reescribe periódicamente en el chip de memoria mediante el proceso de refresco. El refresco se realiza dentro de la DRAM mientras ocurre otro procesamiento. El refresco es una de las razones por las que los chips DRAM son más lentos que la SRAM.

La mayor parte de la memoria de una placa madre es DRAM, pero se puede encontrar una pequeña cantidad de SRAM dentro del procesador, justo fuera del procesador dentro de la carcasa del procesador y, a veces, en la placa madre. La SRAM también se conoce como **memoria caché**. La memoria caché contiene los datos usados con más frecuencia para que la CPU no tenga que volver a los chips DRAM más lentos para obtener los datos. La Figura 6.1 muestra una placa madre con DRAM y un procesador que contiene SRAM.

> Figura 6.1 DRAM y SRAM

Como se señaló en el Capítulo 3, «En la placa madre», para determinar los requisitos de memoria debes considerar el sistema operativo, las aplicaciones y el hardware instalado. La memoria es una de las cosas más críticas de la placa madre que se puede actualizar fácilmente. Empecemos con el módulo de memoria físico.

### Consejo técnico: no olvides el espacio del disco duro ni la memoria de video

La RAM es solo una pieza del rompecabezas. Todas las partes de una computadora —incluidas la RAM, el espacio del disco duro y la memoria de video— deben funcionar juntas para proporcionar un buen rendimiento (óptimo) del sistema.

## Empaquetado físico de la memoria

La memoria que se usa en las placas madre actuales viene en un empaquetado conocido como **módulo de memoria en línea dual (DIMM)**, que tiene 168, 184, 240 o 288 pines. La memoria también puede llamarse *memory stick*, o un técnico podría llamar a un módulo de memoria una *barra de memoria* o simplemente RAM. Las laptops y las impresoras usan un DIMM más pequeño llamado **DIMM de contorno pequeño (SODIMM)**. La Figura 6.2 muestra la progresión del empaquetado de la memoria. La Figura 6.3 muestra un SODIMM.

> Figura 6.2 Chips/módulos de memoria

> Figura 6.3 SODIMM

## Planificación de una instalación de memoria

Ahora que sabes un poco sobre los tipos de memoria, veamos cómo planificar una instalación de memoria. Algunos puntos clave son los siguientes:

- Consulta la documentación del sistema o de la placa madre para ver qué tipo de memoria se admite.
- Determina qué características se admiten.
- Determina cuánta memoria se necesita.
- Determina qué módulo(s) de memoria necesitas y cuántos de ellos.
- Investiga los precios y compra el (los) módulo(s) de memoria que necesitas.

### Planificación de la instalación de memoria: tipos de módulos de memoria

La tecnología ha proporcionado velocidades DRAM más rápidas sin aumentar demasiado el costo. La Tabla 6.1 enumera algunas de las tecnologías de memoria disponibles hoy en día.

**Tabla 6.1 Tipos de módulos de memoria**

| Tecnología | Explicación |
|---|---|
| SDRAM síncrona (SDRAM) | Realiza acceso a memoria por ráfagas muy rápido. Las nuevas direcciones de memoria se colocan en el bus, pero antes de que se complete la recuperación y ejecución de la dirección de memoria anterior. La SDRAM sincroniza su operación con la señal de reloj de la CPU para acelerar el acceso a la memoria. Se usa con DIMM. |
| Doble velocidad de datos (DDR) | A veces llamada DDR SDRAM o DDR RAM. La memoria DDR puede enviar el doble de datos porque estos se transmiten en ambos lados de la señal de reloj (es decir, en los flancos de subida y de bajada en lugar de solo en el flanco de subida). |
| DDR2 | A veces llamada DDR2 RAM. La DDR2 usa DIMM de 240 pines y no es compatible con DDR. |
| DDR3 | Usa DIMM de 240 pines y no es compatible con DDR2 ni DDR. Admiten sistemas basados en procesadores multinúcleo y una utilización de energía más eficiente (1.5). |
| DDR4 | Funciona a un voltaje más bajo (1.2 V) y velocidades más rápidas que los módulos DDR3. La DDR4 usa DIMM de 288 pines y no es compatible con DDR, DDR2 ni DDR3. |
| DDR5 | Funciona a un voltaje más bajo (1.1 V) y velocidades más rápidas que los módulos DDR4. Usa 288 pines como la DDR4, pero no se puede insertar en una ranura DDR4. |

### Consejo técnico: usar un chip de menor voltaje

Los módulos DDR3 y DDR4 se pueden adquirir como un módulo que usa un voltaje más bajo que un módulo estándar. La placa madre debe admitir esta característica. Estos módulos llevan una L al final (DDR4L, por ejemplo).

Aunque todos los módulos DDR tienen diferente número de pines, tienen el mismo tamaño físico. Un módulo DDR5 no cabe en una ranura DDR2, DDR3 o DDR4. La mayoría de las personas no pueden distinguir entre los módulos de memoria DDR. Tienes que asegurarte de tener el tipo correcto de módulo para la placa madre. La Figura 6.4 muestra DIMM DDR4. Observa en la Figura 6.4 la carcasa metálica, llamada **disipador de calor**, en el exterior del módulo de memoria. Comúnmente se usan aluminio o cobre en los disipadores de calor para disipar el calor de la memoria.

> Figura 6.4 DIMM DDR4

### Consejo técnico: usar el tipo correcto de chips de memoria

El chipset y el diseño de la placa madre son muy específicos en cuanto al tipo, la velocidad y las características que pueden tener los chips de memoria. Consulta la documentación de la placa madre.

La Tabla 6.2 enumera algunos ejemplos de modelos de DIMM.

**Tabla 6.2 DIMM**

| Tipo de memoria | Nombre alternativo | Velocidad de reloj | Velocidad de datos |
|---|---|---|---|
| PC3-16000 | DDR3-2000 | 1000 MHz | 2.0 GT/s |
| PC3-17000 | DDR3-2133 | 1066 MHz | 2.13 GT/s |
| PC4-1866 | DDR4-1866 | 933 MHz | 1.86 GT/s |
| PC4-2400 | DDR4-2400 | 1200 MHz | 2.4 GT/s |
| PC4-2666 | DDR4-2666 | 1333 MHz | 2.66 GT/s |
| PC4-3000 | DDR4-3000 | 1500 MHz | 3 GT/s |
| PC4-25600 | DDR4-3200 | 1600 MHz | 3.2 GT/s |

Debido a que un DIMM se puede mostrar con la designación PCX- o DDRX-, el tipo que compres puede resultar confuso. Una breve explicación puede ayudar. DDR3-2000 es un tipo de memoria DDR3 que puede funcionar en un bus frontal de 1000 MHz (el número después de DDR3 dividido por la mitad). Otra forma de mostrar el mismo chip sería usar la designación PC3-16000, que es el ancho de banda teórico del chip de memoria en MB/s. La buena noticia sobre DDR4 y DDR5 es que los nombres de los módulos ahora coinciden con los nombres estándar.

### Planificación de la instalación de memoria: características de la memoria

Además de determinar qué tipo de chips de memoria se van a usar, debes determinar qué características podrían tener los chips de memoria. La documentación del sistema informático o de la placa madre delimita qué características se admiten. La Tabla 6.3 ayuda a caracterizar las características de la memoria.

**Tabla 6.3 Características de la memoria**

| Característica | Explicación |
|---|---|
| Non-parity (sin paridad) | Chips que no usan ninguna verificación de errores. Si un anuncio no dice paridad o ECC, el módulo de memoria es non-parity y del tipo más común. |
| Código de corrección de errores (ECC) | Usa un algoritmo matemático para verificar la exactitud de los datos. La ECC puede detectar errores de memoria de hasta 4 bits y corregir errores de memoria de 1 bit en computadoras de gama alta y servidores de red. |
| Memoria unbuffered (sin búfer) | Memoria en la que los datos se envían inmediatamente a través del chip de memoria. Es lo opuesto a la memoria registrada y es más rápida que la memoria registrada o totalmente con búfer. |
| Memoria buffered (con búfer, memoria registrada) | Un módulo de memoria que tiene chips adicionales (registros) cerca de la parte inferior del módulo que retrasan todas las transferencias de datos para garantizar la exactitud en servidores y computadoras de gama alta. A estos módulos a veces se les llama DIMM totalmente con búfer (FBDIMM). |
| Detección de presencia en serie (SPD) | Un módulo que tiene una EEPROM adicional que contiene información sobre el DIMM (capacidad, voltaje, tasas de refresco, etc.). El BIOS/UEFI lee y usa estos datos para obtener el mejor rendimiento. Algunos módulos tienen sensores térmicos (a veces indicados como TS en los anuncios) que supervisan y notifican las condiciones de calor de la memoria. |
| Memoria de doble voltaje | Un módulo que puede aparecer con una L y que puede funcionar a un nivel de voltaje más bajo (por lo tanto, con menos calor). |
| Perfil de memoria extrema (XMP) | Un módulo que permite al BIOS/UEFI configurar los ajustes de voltaje y temporización para hacer overclocking de la memoria. |

Un módulo de memoria puede usar más de una de las categorías enumeradas en las Tablas 6.2 y 6.3. Por ejemplo, un DIMM podría ser un módulo DDR4, podría estar registrado y podría admitir ECC para la detección y corrección de errores. La mayoría de la memoria registrada también usa la tecnología ECC. Los módulos de memoria pueden admitir ECC o no ECC, y pueden ser registrados o sin búfer. Es importante que investigues esto antes de comprar memoria.

### Consejo técnico: si la corrección de errores no se menciona en el anuncio…

Si no se menciona la corrección de errores, el chip es un chip non-parity. La mayoría de los módulos de memoria actuales son non-parity porque la circuitería del controlador de memoria proporciona la corrección de errores.

## Planificación de la memoria: cuánta memoria instalar

Cuando quieres mejorar el rendimiento de una computadora, agregar memoria es una de las actualizaciones más fáciles. La cantidad de memoria necesaria depende del sistema operativo, de las aplicaciones, del número de aplicaciones abiertas al mismo tiempo, del tipo de computadora y del máximo permitido por la placa madre. Los módulos de memoria vienen en capacidades específicas, como las que se muestran en la Figura 6.5. Observa cómo las capacidades se duplican. Si alguien instalara cuatro módulos de 512 MB, por ejemplo, la cantidad total instalada sería de 2 GB (ya que dos módulos de 512 MB equivalen a 1 GB). Si una placa madre tuviera cuatro ranuras de expansión de memoria y el máximo que admitiera la placa madre fuera de 8 GB, entonces el módulo de memoria de mayor capacidad que podrías colocar en cualquier ranura sería un módulo de 2 GB.

> Figura 6.5 Capacidades de los módulos de memoria

El sistema operativo que uses determina en gran medida el punto de partida para la cantidad de memoria que debes tener. En general, cuanto más antiguo o menos potente sea tu sistema operativo, menor es la cantidad de RAM que necesitas. La Tabla 6.4 proporciona un punto de partida para calcular los requisitos de memoria. Recuerda que cuanto más quieras ejecutar más aplicaciones simultáneamente y mayor sea la función de la aplicación (como juegos o manipulación de fotos/video/sonido), más memoria necesitarás. Ten en cuenta también que las recomendaciones de memoria que se muestran en la Tabla 6.4 no son los requisitos mínimos indicados por los creadores del sistema operativo. Observa que las computadoras Apple (macOS) tienen recomendaciones de memoria similares a las de las PC.

**Tabla 6.4 Recomendaciones de memoria inicial mínima del sistema operativo**

| Sistema operativo | Cantidad mínima de RAM para comenzar los cálculos |
|---|---|
| Windows 10 | 2 GB |
| Windows 11 | 4 GB |
| macOS Sierra/High Sierra/Mojave | 2 GB |
| macOS Sierra/Catalina/Big Sur | 4 GB |
| Linux | Según la versión, a partir de 64 MB |

Al actualizar la memoria, necesitas conocer un par de datos clave:

- ¿Con cuánta memoria empiezas?
- ¿Cuántas ranuras de RAM de la placa madre se están usando actualmente y hay ranuras libres?
- ¿Cuál es la cantidad máxima de memoria que admite tu placa madre?

### Consejo técnico: Windows podría tener limitaciones de memoria

Aunque la placa madre permita más memoria, tu sistema operativo tiene limitaciones. Actualiza el sistema operativo si este es el caso. La Tabla 6.5 muestra los límites de memoria de Windows.

**Tabla 6.5 Límites de memoria de Windows**

| Sistema operativo | Límite de memoria |
|---|---|
| Windows 10 Home | 128 GB |
| Windows 10 Pro/Enterprise | 2 TB |

Para ver la cantidad de memoria instalada, accede a la ventana Información del sistema desde un símbolo del sistema escribiendo `msinfo32` y presionando **Enter**. Desplázate hacia abajo para ver la información de memoria. La Figura 6.6 muestra la ventana Información del sistema de un sistema informático que actualmente tiene 24 GB de RAM instalados (24.0 GB de memoria física total).

> Figura 6.6 Ventana Información del sistema

### Consejo técnico: toda placa madre tiene un máximo

Cada placa madre admite una cantidad máxima de memoria. Debes revisar la documentación de la computadora o de la placa madre para ver cuánto es. No hay solución alternativa para esta limitación. Si quieres más memoria de la que permite la placa madre, debes actualizar a una placa madre diferente.

La Figura 6.7 muestra un anuncio de ejemplo de una placa madre micro-ATX. La pestaña Especificaciones comúnmente muestra el tipo de memoria admitida (y también puede mostrar las velocidades exactas admitidas), la cantidad máxima de memoria y el número de ranuras de memoria.

> Figura 6.7 Especificaciones de memoria de una placa madre de ejemplo

Para determinar cuántas ranuras estás usando actualmente y si tienes alguna libre, debes (1) acceder al BIOS/UEFI para ver esta información; (2) usar la pestaña Rendimiento del Administrador de tareas en Windows; o (3) quitar la cubierta de la computadora y mirar la placa madre para ver qué ranuras de memoria tienen módulos instalados y si hay ranuras libres. Algunos sitios web de venta de memoria tienen un programa de software que determina el tipo de memoria que estás usando y hace recomendaciones.

## Planificación de la memoria: ¿cuántos de cada tipo de memoria?

Una placa madre tiene un número determinado de ranuras de memoria, determinado por su fabricante. El tipo de módulo de memoria que se inserta en una ranura y las características que tiene el módulo están determinados por el fabricante de la placa madre. La mayoría de las placas madre actuales admiten **memoria de doble canal**. El doble canal significa que el chip controlador de memoria de la placa madre maneja el procesamiento de las solicitudes de memoria de manera más eficiente al manejar dos rutas de memoria simultáneamente. Por ejemplo, digamos que una placa madre tiene cuatro ranuras de memoria. Tradicionalmente, el chip controlador de memoria, comúnmente llamado MCH (*memory controller hub*), tenía un canal por el cual viajaban todos los datos de las cuatro ranuras. Con el doble canal, las cuatro ranuras se dividen en dos canales, y cada canal tiene dos ranuras. La Figura 6.8 muestra este concepto.

> Figura 6.8 Memoria de doble canal

El doble canal aumenta el rendimiento de un sistema. Sin embargo, acelera las cosas solo en algunas placas madre si los módulos de memoria coinciden exactamente: mismo tipo de memoria, mismas características de memoria, misma velocidad y misma capacidad. Ten en cuenta que en algunas placas madre los módulos de memoria del Canal A y del Canal B no tienen que tener las mismas capacidades, pero la capacidad total del módulo de memoria del Canal A debe coincidir con la capacidad total de los módulos de memoria instalados en el Canal B. Algunas placas madre requieren esto. La Figura 6.9 ilustra este concepto.

> Figura 6.9 Doble canal

Observa en la Figura 6.9 que, en el primer ejemplo, se insertan dos módulos de memoria idénticos: un módulo de memoria en el Canal A y el otro en el Canal B. Algunos fabricantes de placas madre requieren que los módulos de memoria coincidan en todos los aspectos —fabricante, temporización y capacidad— para admitir el doble canal. Si admiten módulos que no coinciden perfectamente, el canal funcionará con las especificaciones más bajas.

En la sección inferior que se muestra en la Figura 6.9, los cuatro DIMM están instalados. Observa que la capacidad total del Canal A coincide con la capacidad total del Canal B (3 GB en ambos canales, para un total de 6 GB).

### Consejo técnico: el doble canal debe usar pares exactos de módulos de memoria

El Canal A y el Canal B (a veces etiquetados como Canal 0 y Canal 1) deben tener módulos de memoria coincidentes. Compra un kit (un paquete de módulos de memoria previamente probados que están garantizados para funcionar juntos) para asegurarte de que los dos módulos sean iguales.

Para planificar la cantidad correcta de memoria, debes consultar la documentación de la placa madre. Un ejemplo ayuda con este concepto. La Figura 6.10 muestra un diseño de placa madre con cuatro ranuras de memoria que tiene un etiquetado diferente al que se muestra en la Figura 6.9. Recuerda que los fabricantes de placas madre pueden etiquetar sus placas madre como quieran. Esta es una de las razones por las que la documentación es tan importante.

> Figura 6.10 Placa madre con cuatro ranuras de memoria y dos canales

La placa madre de la Figura 6.10 admite DIMM DDR3 sin búfer y no ECC de 512 MB, 1 GB y 2 GB, para un máximo de 8 GB. Supón que el cliente quiere 2 GB de RAM. ¿Qué podrías hacer? ¿Cuántos módulos de memoria comprarías y con qué capacidades? La Tabla 6.6 muestra las posibles soluciones. La mejor solución es la segunda porque tiene los chips de mayor capacidad y aprovecha el doble canal, y todavía quedan ranuras libres para más actualizaciones.

**Tabla 6.6 Posibles soluciones**

| Solución | Número y tamaño de los módulos de memoria necesarios |
|---|---|
| 1 | Cuatro DIMM de 512 MB instalados en las ranuras DIMM1, DIMM2, DIMM3 y DIMM4 (doble canal) |
| 2\* | Dos DIMM de 1 GB instalados en las ranuras DIMM1 y DIMM2 (doble canal) |
| 3 | Dos DIMM de 1 GB instalados en las ranuras DIMM1 y DIMM3 (sin doble canal) |
| 4 | Un DIMM de 2 GB instalado en DIMM1 (sin doble canal) |

\*Mejor solución

Muchas placas madre más nuevas y placas madre de servidor admiten **memoria de triple canal**, donde tres módulos de memoria trabajan juntos, o **memoria de cuádruple canal**, donde se accede a cuatro módulos de memoria simultáneamente. Esta característica se encuentra más comúnmente en placas madre de servidor. La Figura 6.11 muestra una placa madre que tiene seis ranuras de expansión de memoria y que admite triple canal.

> Figura 6.11 Placa madre con seis ranuras de memoria y tres canales

## Planificación de la memoria: investigar y comprar memoria

El paso de investigación y compra en el proceso de planificación de una instalación o actualización de memoria es el paso con más probabilidades de hacerte perder la cabeza. Diferentes sitios web enumeran la memoria de manera diferente. Algunos te dan demasiada información y otros muy poca. Unos pocos, como Kingston Technology (www.kingston.com) y Crucial (www.crucial.com), se especializan en memoria y lo hacen lo más indoloro posible. ¡Incluso proporcionan herramientas que escanean tu computadora y recomiendan actualizaciones de memoria o almacenamiento compatibles! Sin embargo, como técnico, debes estar familiarizado con todos los aspectos de la memoria y los anuncios de memoria.

### Consejo técnico: comprar el tipo de memoria más rápido que permita una placa madre

Comprar memoria más rápida de lo que permite la placa madre es como llevar un auto de carreras por un camino sin pavimentar de un solo carril: el auto tiene la capacidad de ir más rápido, pero no es factible con el tipo de camino que se usa. A veces debes comprar memoria más rápida porque la memoria más antigua ya no se vende. Esto está bien, siempre que sea del tipo correcto, como DDR3, DDR4 o DDR5.

Un aspecto confuso de comprar memoria es la velocidad de la memoria. La velocidad de la memoria se puede representar como MHz o como la clasificación PC. Cuanto mayor sea el número, más rápida será la velocidad del módulo. Para entender mejor la memoria, lo mejor es ver algunos ejemplos. La Tabla 6.7 muestra ejemplos de cómo se podrían anunciar diferentes cantidades de memoria.

**Tabla 6.7 Ejemplos de anuncios de DIMM**

| Módulo de memoria | Cómo podría anunciarse |
|---|---|
| 2 GB | DDR3 PC3-10600 • CL9 • UNBUFFERED • NON-ECC • DDR3-1333 • 1.35V • 256 Megx64 |
| Kit de 2 GB (1 GBx2) | DDR3 PC3-10600 • CL9 • REGISTERED • ECC • DDR3-1333 • 1.5V • 128 Megx72 |
| PC4-17000 | 2133MHz uDIMM single-rank |
| 16 GB (2x8GB) | DDR4 3200MHz Desktop Memory Kit CL16 |

Observa en la Tabla 6.7 cómo los anuncios enumeran el módulo de memoria como DDR4 o PC4 para el tipo DDR4. Si un anuncio no menciona ECC, entonces puedes suponer que la memoria es non-parity y que no hace ninguna verificación de errores. La electrónica actual es muy precisa y, para la mayoría de las aplicaciones no financieras, la memoria non-parity está bien. Si ves uDIMM, es para memoria no registrada o sin búfer.

La segunda y la cuarta fila de la Tabla 6.7 enumeran kits para placas madre que tienen capacidades de doble canal. El kit de 2 GB incluye dos módulos de memoria de 1 GB, para un total de 2 GB de ganancia de memoria. A veces podrías ver las palabras *dual-rank* en un anuncio. Esto es como tener dos módulos combinados en un solo módulo. Estos módulos con frecuencia tienen memoria en ambos lados del módulo. El dual-rank solo funcionará si la placa madre lo admite. La tercera fila menciona un módulo de memoria que es single-rank, lo que simplemente significa que es un módulo de memoria normal.

Otra lista en el anuncio de memoria que se muestra en la Tabla 6.7 es la clasificación CL. **CL** (*column address strobe* [CAS] *latency*, latencia de la señal de selección de columna) es la cantidad de tiempo que pasa antes de que el procesador pase a la siguiente dirección de memoria. La RAM está formada por celdas que contienen datos. Una celda es la intersección de una fila y una columna. (Es muy parecido a una celda en una aplicación de hoja de cálculo.) La señal CAS selecciona qué columna de memoria elegir, y una señal llamada RAS (*row address strobe*, señal de selección de fila) selecciona qué fila elegir. La intersección de las dos es donde se almacenan los datos.

### Consejo técnico: clasificaciones CL y velocidad

Cuanto menor sea la clasificación CL, más rápida será la memoria. Piensa en el tiempo de acceso como en una competencia de atletismo: la persona con el menor tiempo gana la carrera y se considera la más rápida. Los chips con una clasificación CL más baja son más rápidos que los que tienen números más altos.

## Descripción general de la instalación de memoria

La memoria es una parte importante del rendimiento de la computadora. La instalación implica planificar, instalar y posiblemente extraer algunos módulos más antiguos. La falta de planificación puede provocar un rendimiento inferior al óptimo.

El siguiente es el mejor proceso para determinar qué chips de memoria instalar en cada banco:

**Paso 1.** Determina qué capacidades de chip se pueden usar para el sistema. Busca esta información en la documentación incluida con la placa madre o la computadora.

**Paso 2.** Determina cuánta memoria se necesita. Pregunta a los usuarios qué sistema operativo está instalado y qué aplicaciones usan (o averígualo tú mismo). Consulta la documentación de cada aplicación para determinar la cantidad de RAM recomendada. Planifica el crecimiento.

**Paso 3.** Determina la capacidad de los chips que van en cada banco dibujando un diagrama del sistema, planificando la población de memoria en papel y consultando la documentación del sistema o de la placa madre.

Es posible que se deban extraer algunos módulos de memoria para colocar otros de mayor capacidad en el banco. Mira lo que ya está instalado en el sistema, consulta la documentación y extrae los módulos existentes, según sea necesario, para actualizar la memoria.

### Consejo técnico: recordatorio de seguridad con la memoria

Antes de instalar un módulo de memoria, apaga la computadora, desconecta el cable de alimentación de la parte trasera de la computadora y usa procedimientos antiestáticos adecuados. Los módulos de memoria son especialmente susceptibles a la ESD. Si la ESD daña un módulo de memoria, es posible que el problema no aparezca de inmediato y que sea intermitente y difícil de diagnosticar.

## Extracción e instalación de memoria

Al extraer un DIMM, presiona hacia abajo las lengüetas de retención que sujetan el DIMM. Ten cuidado de no forzar demasiado las lengüetas al presionarlas. El DIMM se eleva ligeramente fuera del zócalo. Asegúrate siempre de estar conectado a tierra para evitar la ESD usando una pulsera antiestática o manteniendo el contacto entre una parte descubierta del brazo y el metal dentro de la computadora (**autoconexión a tierra**). La Figura 6.12 muestra los pasos para extraer un DIMM.

> Figura 6.12 Extracción de un DIMM

Un DIMM tiene una o más muescas en la parte inferior, de modo que el módulo se inserta en el zócalo de memoria de una sola manera. Verifica que las muescas en la parte inferior del módulo se alineen con las muescas de la ranura de memoria de la placa madre. El DIMM no se insertará en el zócalo de memoria a menos que esté orientado correctamente.

Asegúrate de que las lengüetas laterales estén hacia afuera antes de insertar el DIMM y cierra las lengüetas sobre el DIMM una vez que esté firmemente insertado en el zócalo. Si el DIMM no entra fácilmente en la ranura, no lo fuerces y verifica la alineación correcta. Una vez que el DIMM esté alineado correctamente en la ranura, empuja el DIMM firmemente dentro de la ranura, y las lengüetas deberían cerrarse naturalmente sobre el DIMM o en los lados del DIMM. La Figura 6.13 ilustra cómo insertar un DIMM. La Figura 6.14 muestra un primer plano de cómo la lengüeta debe encajar firmemente en la muesca del módulo de memoria.

> Figura 6.13 Instalación de un DIMM

> Figura 6.14 Lengüeta segura del DIMM

### Consejo técnico: los códigos de error POST son normales después de una instalación/actualización de memoria

Algunas computadoras muestran un mensaje de error POST o entran automáticamente al programa de configuración. Esto es normal. Lo importante que debes observar durante el POST es que la memoria que se muestra en el BIOS/UEFI debe ser igual a la cantidad de memoria instalada.

Agregar más RAM puede marcar una diferencia notable en el rendimiento de la computadora (hasta cierto punto, por supuesto). Cuando un usuario de computadora está sentado frente a una computadora esperando que aparezca un documento o esperando pasar a una ubicación diferente dentro de un documento, podría ser el momento de instalar más RAM. Si tienes varias aplicaciones abiertas en la barra de tareas, haz clic en una de ellas. Si tienes que esperar varios segundos antes de que aparezca, podría ser una buena idea actualizar tu RAM.

## RAM virtual

La **RAM virtual** (memoria virtual) implica usar el espacio del disco duro como si fuera RAM. La memoria virtual permite al sistema operativo ejecutar aplicaciones más grandes y administrar varias aplicaciones que se cargan simultáneamente. La cantidad de espacio del disco duro usado es dinámica; es decir, aumenta o disminuye según sea necesario. Si el sistema comienza a paginar con frecuencia y está constantemente intercambiando datos de la RAM al disco duro, el tamaño se reduce automáticamente. Consulta la Figura 6.15 y observa cómo cada aplicación tiene su propio espacio de memoria.

> Figura 6.15 Uso de la memoria virtual de Windows

Un **archivo de paginación** es un bloque de espacio del disco duro que las aplicaciones usan como RAM. Otros nombres para el archivo de paginación incluyen pagefile, pagefile.sys, archivo de página y archivo de intercambio (*swap file*). Vuelve a la Figura 6.6, que muestra la pantalla Información del sistema, y podrás ver los datos relacionados con el archivo de paginación junto a Memoria virtual total, Memoria virtual disponible y Espacio del archivo de paginación. Para un rendimiento óptimo en cualquier sistema operativo Windows, reserva tanto espacio libre en el disco duro como sea posible para permitir amplio espacio para la memoria virtual y el almacenamiento en caché. Mantén el disco duro limpio de archivos temporales y archivos/aplicaciones obsoletos.

### Consejo técnico: consejos sobre el archivo de paginación del disco duro

Si hay varios discos duros disponibles, un técnico podría querer mover el archivo de paginación a otra unidad. Coloca siempre el archivo de paginación en el disco duro más rápido, a menos que ese disco duro carezca de espacio.

La cantidad de memoria virtual la crea dinámicamente el sistema operativo y normalmente no necesita configurarse manualmente. En Windows, busca la palabra `performance` > selecciona el vínculo *Adjust the Appearance and Performance of Windows* > pestaña *Advanced* > botón *Change*. Cambia los parámetros y haz clic en OK dos veces. La Figura 6.16 muestra cómo se relaciona la memoria virtual con la RAM y el espacio del disco duro.

> Figura 6.16 Memoria virtual

## Supervisión del uso de memoria en Windows

Windows tiene una utilidad de **Rendimiento** en el Administrador de tareas para supervisar el uso de memoria. Para acceder al Administrador de tareas, presiona **Ctrl** + **Shift** + **Esc**. Selecciona la pestaña Rendimiento, que tiene gráficos que demuestran visualmente el uso de la CPU y la memoria.

La Figura 6.17 muestra el Administrador de tareas, y la Tabla 6.8 detalla algunos de los campos relacionados con la memoria. Ten en cuenta que para ver los datos relacionados con la memoria, debes hacer clic en la opción Memoria en el panel izquierdo. En la sección Composición de memoria hay varias secciones separadas por barras verticales. Puedes colocar el puntero dentro de un espacio y aparecerá el nombre de la sección. Las secciones, de izquierda a derecha, son las siguientes:

**Tabla 6.8 Campos relacionados con la memoria de la pestaña Rendimiento del Administrador de tareas de Windows**

| Campo | Descripción |
|---|---|
| En uso (In Use) | La cantidad de memoria que actualmente usan las aplicaciones, el sistema operativo, los controladores y los procesos. |
| Disponible (Available) | La cantidad de memoria física para uso de las aplicaciones y del sistema operativo. |
| Confirmada (Committed) | Se muestra como dos números. El primer número es cuánta memoria ha identificado el sistema operativo a partir de las aplicaciones y procesos abiertos que necesitan memoria (y que podrían quitarse o paginarse fuera de la RAM si otros procesos más importantes necesitan el espacio). El segundo número es la cantidad de memoria física y virtual disponible. |
| En caché (Cached) | El espacio de memoria que incluye datos que deben escribirse en el disco antes de estar disponibles, así como datos en caché que actualmente no se usan. |
| Grupo paginado (Paged Pool) | Memoria reservada para funciones del sistema operativo o controladores de dispositivos que podrían escribirse en el disco, si es necesario. |
| Grupo no paginado (Non-Paged Pool) | Memoria reservada para funciones del sistema operativo o controladores de dispositivos que deben permanecer en la memoria física (es decir, que no se pueden paginar fuera). |
| Velocidad (Speed) | Velocidad de los chips de RAM. |
| Ranuras usadas (Slots Used) | Número de ranuras de memoria usadas para módulos de memoria y número total de ranuras. |
| Factor de forma (Form Factor) | Tipo de módulo de memoria, como DIMM o SODIMM (usado en laptops). El Capítulo 11, «Computer Design and Troubleshooting Review», cubre los dispositivos móviles y los SODIMM. |
| Reservada para hardware (Hardware Reserved) | Memoria reservada para controladores de dispositivos o firmware que Windows no puede usar para ninguna otra función. |

- **En uso:** la cantidad de memoria que se está usando actualmente
- **Modificada:** memoria que contiene datos que deben escribirse en la unidad antes de que otro elemento pueda usar la ubicación de memoria
- **En espera:** la cantidad de memoria que está en caché y actualmente no se usa
- **Libre:** la memoria disponible para usar

> Figura 6.17 Pestaña Rendimiento del Administrador de tareas de Windows — Memoria

## Aplicaciones anteriores en Windows

Las aplicaciones más antiguas a veces son un desafío en las versiones más nuevas de Windows. Algunas aplicaciones antiguas no funcionan en las versiones más nuevas de Windows porque estos programas con frecuencia hacen llamadas directas al hardware, lo cual Windows 7 y versiones superiores no permiten. Estos programas también pueden requerir que cambies la profundidad de color y la configuración de resolución mediante el Panel de control de Pantalla.

Para Windows 7 y superior, Microsoft afirma que es posible que algunos programas antiguos no se ejecuten correctamente y ofrece el **modo de compatibilidad**. Haz clic con el botón derecho en el icono de la aplicación desde el menú Inicio o haz clic con el botón derecho en el archivo ejecutable del programa y selecciona Propiedades. Usa la pestaña Compatibilidad para seleccionar la versión de Windows para la que se escribió la aplicación. Si no conoces la versión, puedes seleccionar el botón *Run Compatibility Troubleshooter* y luego seleccionar el vínculo *Try Recommended Settings*. La Figura 6.18 muestra la pestaña Compatibilidad.

> Figura 6.18 Pestaña Compatibilidad de Windows

También puedes configurar máquinas virtuales usando software de virtualización como Virtual PC o Hyper-V de Microsoft, Oracle VM VirtualBox o VMware Workstation para ejecutar sistemas operativos más antiguos así como aplicaciones más antiguas. Una **máquina virtual (VM)** te permite reducir los costos de hardware al ejecutar varios sistemas operativos simultáneamente en una sola computadora (sin que uno interfiera con el otro). La virtualización se cubre con más detalle en el Capítulo 12, «Internet Connectivity, Virtualization, and Cloud Technologies».

## Solución de problemas de memoria

Puedes obtener errores de «out of memory» (sin memoria), pitidos POST, luces o códigos de diagnóstico de la placa madre, bloqueos del sistema (apagados intermitentes), rendimiento lento, el molinete giratorio (que indica que una aplicación está bloqueada) y fallos de aplicaciones debido a problemas de memoria. Con cualquiera de estos problemas, sin importar qué sistema operativo se esté usando, verifica la cantidad de memoria disponible y el espacio libre en el disco duro. A veces debes cerrar todas las aplicaciones, reiniciar la computadora y abrir solo la aplicación que se estaba ejecutando cuando ocurrió el error de falta de memoria, porque algunas aplicaciones no liberan el espacio de memoria que ocupan. Usa el Administrador de tareas o la configuración Aplicaciones para detener la aplicación.

Los siguientes consejos y pasos de solución de problemas ayudan con la administración de la memoria:

- Agrega más RAM. Para ver la cantidad de memoria física (RAM) instalada actualmente, accede al Explorador de archivos, haz clic con el botón derecho (o mantén presionado brevemente) en Este equipo y selecciona Propiedades.
- Si acabas de instalar memoria nueva y aparece un error, esto es normal. Entra a la Configuración porque el BIOS/UEFI del sistema sabe que algo ha cambiado.
- Si acabas de instalar memoria nueva y la computadora no arranca, revisa tu instalación presionando con cuidado y con más fuerza el módulo de memoria (después de apagar y quitar la energía, por supuesto) para asegurarte de que el módulo esté completamente asentado en la ranura. Verifica si hay cables sueltos cerca del (de los) módulo(s) de memoria. Asegúrate de estar instalando el tipo de memoria correcto.
- Usa la Herramienta de diagnóstico de memoria de Windows, mediante uno de los siguientes métodos:
  - En Windows, busca con las palabras `memory diagnostic`. Selecciona el vínculo *Windows Memory Diagnostic* (Windows 10).
  - Arranca en el menú de Opciones de arranque avanzadas (presionando **F8** al inicio). Presiona **F10**. Presiona **Tab** para pasar a la sección Herramientas > Herramienta de diagnóstico de memoria de Windows.
  - Usa el disco original del sistema operativo Windows para arrancar la computadora. Ingresa los requisitos de idioma y luego haz clic en el vínculo *Repair Your Computer*. En la ventana Opciones de recuperación del sistema, selecciona Herramienta de diagnóstico de memoria de Windows.
  - Usa el comando `mdsched`.
- Elimina archivos/aplicaciones que ya no necesites y cierra las aplicaciones que no se estén usando. Vacía la Papelera de reciclaje.
- Ajusta el tamaño de la memoria virtual.
- No coloques el archivo de paginación en varias particiones que residan en el mismo disco duro. Usa varios discos duros, si es necesario.
- Coloca el archivo de paginación en una partición de disco duro que no contenga el sistema operativo.
- Coloca el archivo de paginación en el disco duro más rápido.
- Quita el esquema de fondo de escritorio o usa uno simple.
- Ajusta la configuración de Archivos temporales de Internet. Para Microsoft Edge en Windows, busca Internet Explorer (no Microsoft Edge) y selecciona Herramientas > Opciones de Internet > botón Configuración. Ajusta cuánto espacio de unidad se reserva para almacenar en caché páginas web.
- Desfragmenta el disco duro. Consulta el Capítulo 7, «Storage Devices», para conocer los pasos.

### Consejo técnico: actualizar la memoria es una solución fácil

Actualizar la memoria es una de las formas más fáciles de resolver problemas de rendimiento. Ten en cuenta que a veces simplemente debes comprar más RAM, pero deberías probar los consejos mencionados anteriormente antes de recurrir a eso.

Si recibes un mensaje de que faltan datos del dispositivo SPD o que son inconcluyentes, tu placa madre está buscando datos SPD que no puede recibir del módulo de memoria. Si es un módulo nuevo, asegúrate de que admita SPD. Si es un módulo más antiguo, debes reemplazar uno de tus módulos de memoria.

El POST generalmente detecta un problema con un chip de memoria, y la mayoría de los sistemas muestran un código de error o un mensaje. La placa madre también puede contener luces de diagnóstico o un código. En cualquier caso, apaga la computadora, quita la cubierta, presiona cualquier módulo de memoria y reinicia. Otra opción es limpiar las ranuras del módulo de memoria con aire comprimido y volver a instalar el módulo. La clave para una buena solución de problemas del chip de memoria es dividir y vencer. Reduce el problema a un módulo de memoria sospechoso y luego intercambia los bancos, si es posible.

### Consejo técnico: cuando agregar más memoria no ayuda

Los sistemas operativos actuales dependen casi tanto del espacio del disco duro como de la RAM debido a la multitarea. La falta de espacio en el disco duro es casi tan mala como no tener suficiente RAM. Si el sistema sigue funcionando lentamente después de agregar RAM, revisa el espacio usado del disco duro y elimina archivos para liberar espacio, actualiza el almacenamiento de la unidad o agrega otra unidad.

## Almacenamiento extraíble

El almacenamiento extraíble es muy importante para los usuarios hoy en día, para PC, laptops, dispositivos móviles, cámaras y teléfonos inteligentes. La memoria extraíble viene en muchas formas y capacidades. El almacenamiento extraíble común incluye unidades flash y tarjetas de memoria.

La **memoria flash** es un tipo de memoria de estado sólido y no volátil que conserva los datos incluso cuando la computadora está apagada. Los dispositivos de red, los teléfonos inteligentes y las tabletas usan memoria flash para almacenar el sistema operativo y las instrucciones. Algunas tabletas pueden usar medios flash externos para el almacenamiento. Las **unidades de estado sólido (SSD)** también usan memoria flash (consulta el Capítulo 7). Las cámaras digitales usan memoria flash para almacenar fotografías. A diferencia de la DRAM, la memoria flash no tiene que refrescarse y, a diferencia de la SRAM, no necesita energía constante. La Figura 6.19 muestra varios dispositivos de memoria flash.

> Figura 6.19 Memoria flash

Las **unidades flash USB** (a veces llamadas unidades de pulgar, barras de memoria o lápices de memoria) permiten almacenamiento de hasta 1 TB, y se esperan capacidades mayores en el futuro cercano. En la Figura 6.19, los elementos azul y verde lima, así como el dispositivo que tiene un clip, son unidades flash USB, y el resto son almacenamiento para cámaras y grabadoras digitales. Después de conectar una unidad flash a un puerto USB, el sistema operativo le asigna una letra de unidad, y se puede usar el Explorador de archivos para manipular archivos en la unidad.

### Consejo técnico: la causa número uno de falla de una unidad flash es la extracción inadecuada

Cuando termines de usar una unidad flash, haz doble clic en el icono Quitar hardware ubicado en el área de notificación. Es posible que tengas que hacer clic en la flecha hacia la izquierda o hacia arriba para ver este icono. Haz clic en *Safely Remove Hardware and Eject Media*. Selecciona la unidad flash adecuada. Cuando aparezca un mensaje que diga que puedes quitar la unidad de forma segura, retira la unidad flash del puerto USB.

La Figura 6.20 muestra el interior de una unidad flash. El Capítulo 11 entra en más detalle sobre los tipos de memoria flash que se usan con tales dispositivos.

> Figura 6.20 Interior de una unidad flash USB

Las **tarjetas de memoria** contienen memoria flash y se usan en teléfonos celulares, grabadoras digitales, cámaras y prácticamente cualquier tipo de dispositivo móvil que puedas encontrar. La Tabla 6.9 enumera tarjetas de memoria que podrías ver o necesitar instalar.

**Tabla 6.9 Tarjetas de memoria**

| Tipo de almacenamiento | Comentarios |
|---|---|
| CompactFlash (CF) | Introducida por SanDisk; usa memoria flash; no requiere una batería para almacenar fotos una vez que se quita la energía; incluye CF-I y CF-II. |
| SmartMedia | Desarrollada por Toshiba; más pequeña y ligera que CF; hay tarjetas adaptadoras con PC Card/ExpressBus ATA disponibles para transferencias de datos. |
| Memory Stick | Creada por Sony; de tamaño pequeño; se puede leer/escribir con un lector Memory Stick; incluye Memory Stick (MS), Memory Stick Duo (MSD), Memory Stick Micro (M2). |
| Secure Digital | Del tamaño de un sello postal; no requiere energía para retener datos; usa tecnología de memoria flash; admite seguridad criptográfica; los diferentes tipos incluyen SD, miniSD, microSD y SDHC. |
| MMC (tarjeta multimedia) | Un tipo de memoria flash usada en muchos dispositivos portátiles, incluidas las cámaras; funciona en muchos dispositivos que admiten tarjetas SD y es menos costosa; los tipos incluyen MMC, eMMC, RS-MMC, MMCmicro, doble voltaje (DV-MMC), MMCplus, MMC mobile y MiCard. |

Relacionado con el almacenamiento extraíble está la copia de los datos que hay en la tarjeta. Un **lector de tarjetas de memoria** o lector multitarjeta se conecta externamente o está integrado en una computadora o laptop. Un lector tiene varias ranuras que permiten leer diferentes medios de memoria. Estos dispositivos tienen muchos nombres, como lector 15 en 1, lector 8 en 1 o lector 5 en 1 (según cuántas ranuras o tipos diferentes de módulos de memoria acepte el dispositivo). Un lector de tarjetas de memoria reconoce instantáneamente las tarjetas de memoria insertadas, cuyo contenido se puede copiar a la computadora y manipular. A las ranuras de la tarjeta de medios se les asignan letras de unidad accesibles a través del Explorador de archivos. La Figura 6.21 muestra uno de estos lectores.

> Figura 6.21 Lector de tarjetas de memoria

### Consejo técnico: sin letra de unidad

Si el medio no aparece en Windows/Explorador de archivos, es posible que el lector se haya desinstalado temporalmente. Usa la herramienta Quitar hardware de forma segura y expulsar medios en el área de notificación, desconecta el cable del puerto y vuelve a insertarlo para asegurarte de que el sistema operativo reconozca el lector. Si el lector de tarjetas o los puertos siguen no estando disponibles o si están integrados en la computadora, reinicia la computadora.

La memoria es uno de los componentes más críticos de una computadora, y es importante que un técnico conozca bien las diferentes tecnologías de memoria. Debido a que la memoria es una de las actualizaciones más comunes, es importante volverse competente y estar bien informado sobre cómo poblar la memoria.

## Habilidades interpersonales: trabajo en equipo

Los técnicos tienden a no gustar de trabajar en equipos tanto como de trabajar por su cuenta. Gran parte del trabajo de un técnico se hace solo. Sin embargo, un técnico normalmente tiene uno o más colegas, un supervisor y una red de socios involucrados con el trabajo, como proveedores, subcontratistas y ayuda de medio tiempo. Es fácil tener una visión de túnel en un trabajo de soporte técnico y perder de vista la misión del negocio. Muchos trabajos técnicos tienen el propósito principal de generar ingresos: resolver los problemas informáticos y de red de las personas con el fin de ganar dinero. Otros técnicos tienen más un rol de soporte administrativo: planificar, instalar, configurar, mantener y solucionar problemas de las tecnologías que el negocio usa para ganar dinero.

Los técnicos deben centrarse en resolver los problemas de los clientes y asegurarse de que los clientes sientan que sus problemas se han resuelto de manera profesional y eficiente. Sin embargo, no puedes perder de vista la mentalidad de «primero el negocio»; recuerda que desempeñas un papel de soporte ya sea que generes ingresos o no. Eres una cifra en el balance general de alguien, y necesitas mantener tus habilidades y actitudes finamente ajustadas para ser valioso para la empresa. No importa lo bueno que seas en tu trabajo, siempre eres mejor para una empresa si formas parte de un equipo que si estás por tu cuenta. Asegúrate de llegar a tiempo, mantener una actitud positiva y proyectar confianza. Ser una persona que llega tarde, se va temprano, conversa demasiado con los clientes, culpa a los demás, etc., no es ser un buen miembro del equipo. Si vas a llegar tarde al trabajo o a irte temprano, informa a tu supervisor y a tus compañeros de trabajo para que puedan ocuparse de cualquier problema que surja mientras no estés. Si vas a llegar tarde a una cita con un cliente, comunícate con el cliente e infórmale que llegarás tarde.

Los técnicos deben ser buenos jugadores de equipo y verse a sí mismos como un reflejo de su empresa cuando están en el trabajo (ver la Figura 6.22). Los empleadores consideran el trabajo en equipo como una parte importante del conjunto de habilidades de un técnico, tan importante como las habilidades técnicas. Piensa en formas de practicar el trabajo en equipo incluso como estudiante y perfeccionar esas habilidades cuando te incorpores al mundo laboral.

> Figura 6.22 Trabajo en equipo

## Resumen del capítulo

- La memoria de una placa madre es SDRAM, un tipo de RAM que es más barata y más lenta que la SRAM, el tipo de memoria que está dentro de la CPU y la carcasa del procesador.
- Cada tipo de módulo DDR solo encajará en la ranura de placa madre de ese tipo de módulo. Por ejemplo, un módulo DDR5 requiere una ranura DDR5.
- La memoria unbuffered non-parity es la memoria que normalmente se instala en las computadoras.
- La ECC se usa para la verificación de errores y se encuentra comúnmente en computadoras de gama alta y servidores.
- La clasificación CL o el primer número de la secuencia de temporización muestra con qué rapidez el procesador puede acceder a los datos en ubicaciones de memoria secuenciales. Cuanto menor sea el primer número, más rápido será el acceso.
- SPD es una tecnología que se usa para que el módulo de memoria pueda comunicar especificaciones al BIOS/UEFI.
- La memoria dual-rank es un módulo que actúa como dos módulos. La memoria single-rank es lo normal, y un anuncio normalmente no usará este término.
- Antes de instalar memoria, planifica tu estrategia: lee el manual para determinar el tipo de memoria; determina la cantidad total de memoria; determina si se debe quitar alguna memoria; determina la memoria que hay que comprar; y ten en cuenta aprovechar al máximo la memoria implementando doble, triple o incluso cuádruple canal.
- Al implementar doble, triple o cuádruple canal, compra módulos de memoria coincidentes.
- Determinadas versiones de Windows tienen limitaciones de memoria.
- La RAM es muy susceptible a los eventos de ESD. Usa procedimientos de manejo adecuados, incluido el uso de una pulsera antiestática.
- Antes de extraer o instalar memoria, desconecta el cable de alimentación y quita la batería en un dispositivo móvil.
- Tener la mayor cantidad de RAM posible en un sistema es un factor de rendimiento importante, y también lo es tener espacio libre en el disco duro, porque el espacio del disco duro se usa como memoria. Esto se llama memoria virtual, y la información que se almacena temporalmente en un disco duro se guarda en un área conocida como archivo de paginación, archivo de página o archivo de intercambio. El archivo de paginación debe estar en la unidad más rápida que tenga el mayor almacenamiento libre.
- Usa el Administrador de tareas para supervisar el rendimiento de la memoria.
- Usa el POST, los códigos de salida de LED/pantalla de la placa madre, los diagnósticos del BIOS/UEFI y la Herramienta de diagnóstico de memoria de Windows para diagnosticar problemas de memoria.
- Los medios flash se usan para proporcionar memoria o espacio de almacenamiento adicional a los dispositivos informáticos e incluyen las unidades flash USB.
- Un técnico es parte de un negocio y debe contribuir al equipo. Un técnico debe representar profesionalmente a una empresa.

## Consejos para el examen de certificación A+

- Sé capaz de instalar la RAM correcta. Conoce los números de pines de DDR3, DDR4 y DDR5 tanto para DIMM como para SODIMM, y que un zócalo DDR3, por ejemplo, no aceptará un módulo DDR4 o DDR5.
- Ten en cuenta que agregar memoria es una de las formas más fáciles de mejorar el rendimiento de la computadora.
- Aprende a calcular qué memoria se necesita para una actualización o una instalación nueva.
- Sé capaz de identificar las ranuras de memoria en una placa madre.
- Aprende a poblar la memoria cuando se implementa doble, triple o cuádruple canal.
- Al poblar la memoria, consulta la documentación de la placa madre antes de continuar.
- Sé capaz de describir la diferencia entre la memoria non-parity y la memoria con código de corrección de errores (ECC).
- Ten en cuenta que los chips de memoria son especialmente susceptibles a la ESD y cómo prevenir el daño por ESD al instalar o extraer memoria. Revisa el Capítulo 5, «Disassembly and Power», para obtener consejos sobre el manejo de la ESD.
- Recuerda que si alguna aplicación responde lentamente, es posible que la computadora necesite más RAM. Los códigos de error POST, los fallos de aplicaciones y los apagados intermitentes pueden indicar un problema de memoria.
- Revisa los síntomas y consejos de solución de problemas al final del capítulo.
- Aprende cuándo y cómo usar el modo de compatibilidad y la Herramienta de diagnóstico de memoria de Windows.
- Ten en cuenta que las siguientes habilidades de profesionalismo son parte del examen 220-1102: (1) mantener una actitud positiva, (2) proyectar confianza, (3) llegar a tiempo y (4) si vas a llegar tarde, comunicarte con el cliente.

## Términos clave

- application crash — *application crash* (fallo de la aplicación)
- be on time — *be on time* (llegar a tiempo)
- buffered memory — *buffered memory* (memoria con búfer)
- cache memory — *cache memory* (memoria caché)
- CL rating — *CL rating* (clasificación CL)
- Compatibility mode — *Compatibility mode* (modo de compatibilidad)
- DDR3 — *DDR3*
- DDR4 — *DDR4*
- DDR5 — *DDR5*
- DIMM — *DIMM* (módulo de memoria en línea dual)
- DRAM — *DRAM* (RAM dinámica)
- dual-channel — *dual-channel* (doble canal)
- ECC — *ECC* (código de corrección de errores)
- flash drive — *flash drive* (unidad flash)
- flash memory — *flash memory* (memoria flash)
- heat spreader — *heat spreader* (disipador de calor)
- intermittent shutdown — *intermittent shutdown* (apagado intermitente)
- maintain a positive attitude — *maintain a positive attitude* (mantener una actitud positiva)
- memory card — *memory card* (tarjeta de memoria)
- memory card reader — *memory card reader* (lector de tarjetas de memoria)
- non-parity — *non-parity* (sin paridad)
- paging file — *paging file* (archivo de paginación)
- Performance utility — *Performance utility* (utilidad Rendimiento)
- pinwheel — *pinwheel* (molinete giratorio)
- POST beep — *POST beep* (pitido POST)
- project confidence — *project confidence* (proyectar confianza)
- quad-channel — *quad-channel* (cuádruple canal)
- RAM — *RAM* (memoria de acceso aleatorio)
- sluggish performance — *sluggish performance* (rendimiento lento)
- SODIMM — *SODIMM* (DIMM de contorno pequeño)
- SPD — *SPD* (detección de presencia en serie)
- SRAM — *SRAM* (RAM estática)
- teamwork — *teamwork* (trabajo en equipo)
- triple-channel — *triple-channel* (triple canal)
- unbuffered memory — *unbuffered memory* (memoria sin búfer)
- virtual machine — *virtual machine* (máquina virtual)
- virtual RAM — *virtual RAM* (RAM virtual)
- Windows Memory Diagnostic Tool — *Windows Memory Diagnostic Tool* (Herramienta de diagnóstico de memoria de Windows)

## Preguntas de repaso

Las siguientes especificaciones de RAM de placa madre se usan para las preguntas 1 a 5:

- Cuatro zócalos DIMM DDR4 SDRAM dispuestos en dos canales y que admiten hasta 128 GB (32 GB de capacidad por DIMM individual) de memoria del sistema
- Compatibilidad con módulos de memoria DIMM DDR4 3200/2933/2667/2400/2133 MHz
- Compatibilidad con módulos de memoria DIMM ECC sin búfer 1Rx8/2Rx8
- Compatibilidad con módulos de memoria DIMM no ECC sin búfer 1Rx8/2Rx8/1Rx16
- Compatibilidad con módulos de memoria de perfil de memoria extrema (XMP)
- Compatibilidad con hasta 16 GB de memoria del sistema

1. De las características dadas, ¿cuál(es) se aplicaría(n) a esta computadora? (Elige todas las que correspondan.)
   [ unbuffered | registered | SO-DIMM de 204 pines | DIMM DDR5 de 288 pines | DIMM DDR4 de 288 pines | ECC | non-ECC | single rank | dual rank ]

2. Supón que esta computadora tiene 4 GB de memoria instalados. Escribe todas las combinaciones de población de memoria en las ranuras.
   (1) cuatro módulos de 1 GB, (2) dos módulos de 2 GB, (3) un módulo de 4 GB

3. [ V | F ] El técnico que recomienda memoria para esta placa madre podría recomendar memoria que no realice verificación de errores.

4. ¿Qué significa la afirmación «cuatro zócalos DIMM DDR4 SDRAM dispuestos en dos canales»?

5. ¿Habría algún problema si esta placa madre contuviera 6 GB de RAM y la computadora tuviera Windows 10 de 32 bits instalado? Si es así, explica el problema.

Considera los siguientes anuncios de memoria para computadoras de escritorio que se usan en las preguntas 6 a 11:

a. 2 GB 240-pin SDRAM DDR3L 1600 (PC3L 12800) Desktop Memory
b. 4 GB DDR3-1600 (PC3-12800) CL11 240-pin DIMM
c. 4 GB ECC registered DDR3 SDRAM CAS latency 9
d. 4 GB 240-pin DDR3 SDRAM 1333 (PC3 10600) CAS 9
e. 8 GB (1x8 GB) 1333MHz PC3-10600 CL9 ECC registered dual-rank low power
f. 8 GB (2x4 GB) DDR4 SDRAM 2133 (PC4 17000)
g. 16 GB PC4L-2666
h. 16 GB kit (2x8 GB) DDR4 2666 MHz PC4-21300 CL19 unbuffered non-ECC 1.2V UDIMM
i. 16 GB 1Rx16 DDR4 UDIMM 3200MHz

6. En estos anuncios, ¿qué opción(es) DDR4 contendría la mayor cantidad de datos en un solo módulo de memoria y sería la más adecuada para una computadora de escritorio?

7. En la opción g, ¿qué significa la L en DDR4L?

8. Un cliente quiere 8 GB de RAM con doble canal en una computadora de escritorio. ¿Qué módulo(s) de memoria sería lo mejor comprar, dada la siguiente documentación del manual de la placa madre? (Las ranuras del módulo de memoria están en orden desde la más cercana a la CPU: 1, 3, 2 y 4.)
   - No instales módulos de memoria ECC.
   - Las configuraciones de memoria son las siguientes:
     - Un par de módulos coincidentes en los conectores DIMM 1 y 2
     - Un par de módulos coincidentes en los conectores DIMM 1 y 2 y otro par en los conectores 3 y 4
     - Si instalas pares mixtos, los módulos de memoria funcionan a la velocidad del módulo de memoria más lento instalado.

9. Considerando la respuesta dada a la pregunta 8, ¿qué conectores DIMM de la placa madre se usarían?

10. ¿Qué tipo de característica de memoria se necesitará si la precisión de los datos es primordial para una computadora nueva?
    [ buffered | ECC | registered | XMP ]

11. Al comparar las opciones b y d e imaginar que ambos módulos cuestan lo mismo, ¿cuál sería la mejor compra? Explica tu razonamiento.

12. ¿Qué método es el más eficaz para prevenir un evento de ESD al instalar RAM?
    a. colocar la computadora sobre un tapete antiestático
    b. usar una pulsera antiestática
    c. permanecer en contacto con una parte metálica no pintada de la computadora
    d. usar zapatos con suela de goma y usar el sistema de compañero haciendo que otro técnico esté cerca

13. ¿Cuál de los siguientes sería la primera señal de que una computadora necesita más RAM?
    a. La computadora responde lentamente.
    b. La computadora hace un ruido de tic tac.
    c. Aparece un mensaje de error POST.
    d. Aparece una recomendación de usar la Herramienta de diagnóstico de memoria de Windows.

14. ¿Cómo puedes saber la cantidad máxima de memoria que puede admitir una placa madre?
    a. Mira las opciones de memoria en el BIOS/UEFI.
    b. Usa la pestaña Rendimiento del Administrador de tareas de Windows.
    c. Usa la herramienta Memoria de Windows.
    d. Consulta la documentación de la placa madre.

15. Enumera una forma fácil de saber cuánta RAM está instalada en una computadora.

16. [ V | F ] Un DIMM DDR4 puede caber en una ranura de expansión de memoria DDR3.

17. Acabas de agregar dos módulos de memoria nuevos a una computadora, pero ahora el sistema no arranca y emite varios pitidos. ¿Qué revisarás primero?

18. Da un ejemplo de cómo un técnico podría proyectar confianza mientras trabaja en un servicio de ayuda (*help desk*).

19. Un sistema ya tiene dos módulos de memoria de 2666 MHz instalados, y un técnico agrega dos módulos más que funcionan a 3200 MHz. ¿Cuál será el resultado de esta acción?
    a. La computadora no arrancará.
    b. La computadora podría congelarse a veces.
    c. La memoria funcionará a la velocidad de 2666 MHz.
    d. Toda la memoria funcionará a la velocidad de 3200 MHz.

20. Un técnico ha recibido la queja de que una computadora no funciona tan bien como antes. ¿Qué herramienta de Windows 10 haría que el técnico le pidiera al usuario abrir para saber rápidamente cuánta RAM están usando actualmente las aplicaciones abiertas?
    [ Performance Monitor | Device Manager | System Information Tool | Task Manager ]

## Ejercicios

### Ejercicio 6.1 Configurar la memoria en papel

**Objetivo:** Ser capaz de determinar la cantidad y el tipo correctos de memoria para instalar en una placa madre

**Partes:** Acceso a Internet o acceso a revistas o anuncios que muestren precios de memoria

**Procedimiento:** Consulta la Tabla 6.10 para responder las preguntas. Esta placa madre admite módulos de memoria DDR3 de 1600/1333/1066 MHz. Las capacidades admitidas son 1, 2, 4 y 8 GB, para un total de 16 GB como máximo. La velocidad del canal de memoria está determinada por el DIMM más lento poblado en el sistema.

**Tabla 6.10 Combinaciones single-/dual-channel de la placa madre**

> Nota del traductor: esta tabla es una figura de baja resolución en el original. Su estructura reconstruida es: una fila de encabezado superior con «Sockets» sobre las columnas de DIMM, seguida de la fila de encabezados de columna «Mode | Scenario | DIMM1 | DIMM2» y las filas de datos «Single | 1 | Populated» y «Dual-channel | 2 | Populated | Populated».

|  |  | Sockets |  |
|---|---|---|---|
| Mode | Scenario | DIMM1 | DIMM2 |
| Single | 1 | Populated |  |
| Dual-channel | 2 | Populated | Populated |

1. ¿Qué módulos de memoria se necesitan si el cliente quiere 5 GB de RAM? ¿Qué capacidades y cuántos módulos de cada capacidad se requieren?

2. ¿Cuántas ranuras de memoria tiene esta placa madre? [ 1 | 2 | 3 | 4 ]

3. Usando Internet, una revista de partes de computadora o una lista de módulos de memoria, determina los números de parte exactos y las cantidades de módulos de memoria que comprarías para poblar esta placa madre con 5 GB de RAM. Enlístalos, así como el lugar donde obtuviste la información.

4. Esta placa madre ya tiene 4 GB de RAM instalados en la ranura DIMM1. El cliente quisiera actualizar a 8 GB de memoria total, usar el módulo existente si es posible y usar doble canal. Esta pregunta requiere dos respuestas. ¿Qué capacidad y número de módulos de memoria se necesitan para llegar al total de 8 GB? Enumera cualquier consideración a tener en cuenta.

5. ¿Qué ranura de memoria se usará para instalar el módulo de memoria, según la documentación proporcionada?

6. ¿Qué significa la documentación cuando hace referencia a RAM DDR3 1600/1333/1066 MHz?

7. ¿Cómo sabes cuál de los módulos de 1600, 1333 o 1066 usar?

8. Usando Internet, una revista de partes de computadora o una lista proporcionada de módulos de memoria, determina los números de parte exactos y las cantidades de módulos de memoria que comprarías para llevar esta computadora de 4 GB a 8 GB. Enumera la información del módulo junto con el lugar donde obtuviste la información.

### Ejercicio 6.2 Configurar la memoria en papel

**Objetivo:** Ser capaz de determinar la cantidad y el tipo correctos de memoria para instalar en una placa madre

**Partes:** Acceso a Internet o acceso a revistas o anuncios que muestren precios de memoria

**Procedimiento:** Consulta la Figura 6.23 y la Tabla 6.11 para responder las preguntas. Esta placa madre admite las siguientes configuraciones de memoria:

- Hasta 64 GB de memoria
- Compatibilidad con módulos de memoria DDR4 26666/2400/2133 MHz
- Compatibilidad con módulos de memoria DIMM ECC sin búfer 1Rx8/2Rx8 (funcionan en modo no ECC)
- Compatibilidad con módulos de memoria DIMM no ECC sin búfer 1Rx8/2Rx8/1Rx16

La placa de escritorio admite configuraciones de memoria de canal único o doble. La placa tiene cuatro conectores DIMM DDR4 SDRAM con contactos chapados en oro.

> Figura 6.23 Placa madre con cuatro ranuras de memoria y dos canales

**Tabla 6.11 Guías single-/dual-channel de la placa madre**

| Memoria instalada | Directrices |
|---|---|
| 2 DIMM en doble canal | Instala un par de DIMM coincidentes, iguales en velocidad y tamaño, en DIMM0 de ambos canales, Canal A y Canal B. |
| 4 DIMM en doble canal | Sigue las instrucciones para dos DIMM y agrega otro par de DIMM coincidentes en DIMM1 de ambos canales, A y B. |
| 3 DIMM en doble canal | Instala un par de DIMM coincidentes, iguales en velocidad y tamaño, en DIMM0 y DIMM1 del Canal A. Instala un DIMM igual en velocidad y tamaño total a los DIMM instalados en el Canal A, en DIMM0 o DIMM1 del Canal B. |
| Canal único | Todas las demás configuraciones de memoria dan como resultado el funcionamiento de la memoria en canal único. |

1. Dentro de la documentación, ¿qué significa 1Rx8/2Rx8/1Rx16?

2. ¿Qué características de memoria, si las hay, se pueden usar? (Elige todas las que correspondan.)
   [ non-ECC | non-parity | ECC | registered | fully buffered | unbuffered | SPD ]

3. ¿Qué módulos de memoria se necesitan si el cliente quiere 32 GB de RAM con doble canal? (¿Qué capacidades y cuántos de cada capacidad se requieren?)

4. ¿Qué ranuras de memoria se usarán para instalar los 32 GB de memoria con doble canal, según la información proporcionada?

5. Esta pregunta requiere dos respuestas. Usando Internet, una revista de partes de computadora o una lista de módulos de memoria, determina los números de parte exactos y las cantidades de módulos de memoria que comprarías para poblar esta placa madre con 32 GB de RAM. Enlístalos, junto con el lugar donde obtuviste la información.

6. ¿Qué significa unbuffered?

7. Esta pregunta requiere dos respuestas. ¿Se pueden usar módulos de memoria DDR3 con esta placa madre? ¿Cómo puedes saberlo?

8. Si esta placa madre ya tiene 8 GB de RAM instalados en la ranura DIMM0_ChanA y el cliente quisiera actualizar a 16 GB de RAM con doble canal, ¿qué módulos de memoria se necesitan? (¿Qué capacidades y cuántos de cada capacidad se requieren?)

9. ¿Qué consideraciones tendrías con respecto al doble canal antes de investigar los precios?

10. ¿Qué ranuras de memoria se usarán para instalar los 16 GB de memoria total, según la información proporcionada y el escenario de actualización presentado en la pregunta 8?

11. Usando Internet, una revista de partes de computadora o una lista de módulos de memoria, determina los números de parte exactos y las cantidades de módulos de memoria que comprarías para llegar al total de 16 GB (desde 8 GB) y hacer doble canal. Enlístalos, junto con el lugar donde obtuviste la información.

### Ejercicio 6.3 Configurar la memoria en papel

**Objetivo:** Ser capaz de determinar la cantidad y el tipo correctos de memoria para instalar en una placa madre

**Partes:** Acceso a Internet o acceso a revistas o anuncios que muestren precios de memoria

**Procedimiento:** Consulta la Figura 6.24 para responder las preguntas. La placa madre admite las siguientes configuraciones de memoria:

- Se pueden usar DIMM DDR3 de 1 GB, 2 GB y 4 GB sin búfer y no ECC en las ranuras DIMM (1, 2, 3 y 4) para un total de 32 GB como máximo usando módulos DDR3 de 1066/1333 MHz.
- Las configuraciones de memoria recomendadas son módulos en DIMM1 y DIMM3 o módulos en DIMM1, DIMM2, DIMM3 y DIMM4.
- Se admiten modos de canal único y doble.
- Puedes instalar tamaños diferentes en el Canal A y el Canal B. La configuración de doble canal será el tamaño total del canal de menor tamaño. Cualquier memoria excedente funcionará en modo de canal único.
- Se recomiendan DIMM de >1.65 V.
- Usa la misma latencia CAS y obtén los módulos del mismo proveedor, si es posible.
- La frecuencia de operación de memoria predeterminada depende de SPD.

> Figura 6.24 Segunda placa madre con cuatro ranuras de memoria y dos canales

1. ¿Qué características de memoria, si las hay, se usan? (Elige todas las que correspondan.)
   [ parity | non-parity | ECC | registered | unbuffered | SPD ]

2. El cliente quiere 4 GB de RAM. ¿Qué módulos de memoria se necesitan? (¿Qué capacidades y cuántos de cada capacidad se requieren?)

3. ¿Qué ranuras de memoria se usarán para instalar la memoria sugerida en la pregunta 2?

4. Usando Internet, una revista de partes de computadora o una lista de módulos de memoria proporcionada por el instructor, determina los números de parte exactos y las cantidades de módulos de memoria que comprarías. Enlístalos, junto con el lugar donde obtuviste esta información.

5. ¿En qué tipo de sistemas sería más probable que se requieran y se usen módulos ECC?
   [ escritorio de estudiante | teléfonos inteligentes | tabletas | servidores | laptops ]

6. ¿Cuál es el propósito de los módulos ECC?

7. ¿Cuál es el propósito de SPD?

### Ejercicio 6.4 Configurar la memoria en papel

**Objetivo:** Ser capaz de determinar la cantidad y el tipo correctos de memoria para instalar en una placa madre

**Partes:** Acceso a Internet o acceso a revistas o anuncios que muestren precios de memoria

**Procedimiento:** Consulta la Figura 6.25 para responder las preguntas. La placa madre admite las siguientes configuraciones de memoria:

- Memoria máxima admitida: 16 GB
- Tipos de memoria: DDR4-4600/4400/4266/4200
- Canales de memoria: 3
- Número de DIMM: 4
- ECC admitido: Sí
- Los conectores usan contactos chapados en oro
- DIMM SPD sin búfer y no registrados, de una o dos caras, con una clasificación de voltaje de 1.65 V o menos
- Se puede lograr un rendimiento óptimo instalando tres DIMM coincidentes en las ranuras de memoria ChanA, ChanB y ChanC.
- Se puede lograr el funcionamiento de doble canal instalando DIMM coincidentes en ChanB y ChanC o en las cuatro ranuras de memoria.

> Figura 6.25 Placa madre de triple canal

1. ¿Qué características de memoria, si las hay, se usan? (Elige todas las que correspondan.)
   [ parity | non-parity | ECC | registered | unbuffered | SPD ]

2. El cliente quiere 8 GB de RAM realizando triple canal. ¿Se puede hacer? ¿Por qué sí o por qué no? [ Sí | No ]

3. ¿Qué módulos de memoria se necesitan para poner 8 GB de memoria en la placa madre? (¿Qué capacidades y cuántos de cada capacidad se requieren?) Justifica tu elección.

4. ¿Qué ranuras de memoria se usarán para instalar la memoria sugerida en la pregunta 3?

5. Usando Internet, una revista de partes de computadora o una lista de módulos de memoria proporcionada por el instructor, determina los números de parte exactos y las cantidades de módulos de memoria que comprarías. Enlístalos, junto con el lugar donde obtuviste esta información.

6. El usuario tiene Windows 10 de 32 bits instalado en esta computadora. ¿Habrá algún problema con los 8 GB de RAM? Si es así, ¿cuáles podrían ser esos problemas?

7. Enumera un método que un técnico podría usar para asegurarse de que el sistema reconozca los 8 GB.

## Actividades

### Descubrimiento en Internet

**Objetivo:** Familiarizarse con la investigación de chips de memoria usando Internet

**Partes:** Una computadora con acceso a Internet

**Procedimiento:** Usa Internet para completar el siguiente procedimiento:

- Enciende la computadora e inicia un navegador de Internet.
- Usando cualquier motor de búsqueda, localiza dos proveedores que vendan chips de memoria.
- Crea una tabla como la de abajo y completa tus hallazgos para cada uno de los sitios de memoria.

### Habilidades interpersonales

**Objetivo:** Mejorar y perfeccionar la capacidad de un futuro técnico para escuchar, comunicarse en forma escrita y oral, y apoyar de manera profesional a las personas que usan computadoras

**Actividades:**

1. Por tu cuenta, usa Internet para encontrar una utilidad que evalúe habilidades interpersonales o tu personalidad. Compara tus puntajes con los de otros en la clase. Haz una lista de cómo podrías mejorar en áreas específicas en las que estés débil. Presenta tus hallazgos a un grupo y comparte los hallazgos de tu grupo con otro grupo.

2. Ten en cuenta que esta actividad requiere dos computadoras. En grupos de dos, haz que una persona le describa con gran detalle a la otra cómo actualizar la memoria de la computadora extrayendo memoria de una computadora y agregándola a la otra. La persona que realiza la instalación física no puede hacer nada excepto lo que la pareja describe cómo hacerlo. Invierte los roles para extraer la memoria y volver a instalarla en la computadora original. Al final del ejercicio, los dos participantes describen al maestro lo que experimentaron.

3. En grupos pequeños, encuentren un video que describa cómo hacer algo en una computadora. Evalúen el video en términos de cómo el orador podría hacer un mejor trabajo comunicándose con personas que no son técnicos. Compartan el video con la clase, junto con sus recomendaciones para hacerlo mejor. Como opción, escriban el guion de una breve presentación sobre cómo hacer algo. Grábenla si es posible y hagan que la clase evalúe la presentación de cada grupo.

### Habilidades de pensamiento crítico

**Objetivo:** Analizar y evaluar información, así como aplicar la información aprendida a situaciones nuevas o diferentes

**Actividades:**

1. Usando la documentación de cualquier computadora, compara y contrasta dos escenarios/soluciones de doble canal para un cliente imaginario. Enumera tres recomendaciones que tendrías para el cliente. Escribe una lista de tus hallazgos y compártela con la clase.

2. Enumera las repercusiones de descubrir que una placa madre admite módulos de memoria tanto single-rank como dual-rank. ¿Cómo se compara un módulo de memoria single-rank con un módulo de memoria dual-rank?

3. Descarga un manual de placa madre de Internet o usa uno proporcionado en el aula. Encuentra la sección de memoria y haz una lista de cualquier término o instrucción que se dé y que no entiendas. En grupos de cuatro o cinco, compartan sus listas y propongan tantas soluciones como sea posible. Compartan la lista de su grupo con la clase. Escriban cualquier pregunta sin resolver en el pizarrón y traigan las respuestas a esas preguntas en una semana.
