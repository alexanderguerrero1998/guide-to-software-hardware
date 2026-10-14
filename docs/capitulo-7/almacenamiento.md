# Capítulo 7. Dispositivos de almacenamiento

> Traducción al español del Capítulo 7 («Storage Devices») de *Complete A+ Guide to IT Hardware and Software: CompTIA A+ Exams 220-1101 & 220-1102* (Cheryl A. Schmidt, Christopher Lee) — material de estudio de uso personal.
>
> Nota: las figuras del libro son imágenes y no se incluyen aquí; se conserva su leyenda traducida como referencia. Las tablas se transcriben como tablas de Markdown.

En este capítulo aprenderás:

- Los términos básicos de almacenamiento
- Acerca de las tecnologías IDE (PATA), SATA, eSATA, SSD y SSHD
- Cómo instalar y configurar dispositivos de almacenamiento, incluido RAID
- Cómo solucionar problemas de dispositivos de almacenamiento
- Cómo mantener una unidad en buen estado
- Cómo crear y solucionar problemas de una matriz RAID
- Cómo crear y usar Espacios de almacenamiento de Windows (Windows Storage Spaces)
- Comunicación telefónica eficaz

**Objetivos del examen CompTIA:**

- 1101-3.1 Explicar los tipos básicos de cables y sus conectores, características y propósitos.
- 1101-3.3 Dado un escenario, seleccionar e instalar dispositivos de almacenamiento.
- 1101-5.3 Dado un escenario, resolver y diagnosticar problemas con unidades de almacenamiento y matrices RAID.
- 1102-1.2 Dado un escenario, usar la herramienta de línea de comandos de Microsoft adecuada.
- 1102-1.3 Dado un escenario, usar características y herramientas del sistema operativo (SO) Microsoft Windows 10.
- 1102-1.8 Explicar los tipos comunes de SO y sus propósitos.
- 1102-1.9 Dado un escenario, realizar instalaciones y actualizaciones de SO en un entorno de SO diverso.
- 1102-2.8 Dado un escenario, usar métodos comunes de destrucción y eliminación de datos.
- 1102-3.1 Dado un escenario, solucionar problemas comunes del SO Windows.
- 1102-4.7 Dado un escenario, usar técnicas de comunicación y profesionalismo adecuadas.

## Descripción general de los dispositivos de almacenamiento

Los dispositivos de almacenamiento guardan los datos que tanto nos gusta generar y conservar: fotos, PDF, películas, documentos, hojas de cálculo y cualquier otra cosa que se nos ocurra guardar. Los datos pueden almacenarse en medios ópticos, medios flash o medios magnéticos como los discos duros, como se muestra en la Figura 7.1.

> Figura 7.1 Dispositivos de almacenamiento

Muchas personas, especialmente las que viajan con frecuencia, usan servidores de almacenamiento de datos en su empresa. Los datos también pueden almacenarse «en la nube». Esto significa que hay dispositivos de almacenamiento disponibles en servidores remotos para guardar datos. Parte del almacenamiento lo proporciona un proveedor de internet o como servicio para un dispositivo móvil. Empresas como Amazon, Microsoft, Google, SugarSync y Dropbox ofrecen almacenamiento en la nube. Algunas empresas cobran por el almacenamiento en la nube y otras ofrecen cantidades limitadas de almacenamiento en la nube de forma gratuita y tienen la opción de pagar por más. Esto se conoce como almacenamiento en la nube o almacenamiento remoto (offsite). En el Capítulo 12, «Conectividad a internet, virtualización y tecnologías en la nube», se proporciona más información sobre cómo hacer esto. La Figura 7.2 ilustra este concepto, pero ten en cuenta que «en la nube» no es más que un montón de discos duros, servidores y otros dispositivos en algún lugar remoto.

> Figura 7.2 Almacenamiento en la nube

## Descripción general del disco duro

Un disco duro se puede montar dentro de la carcasa de una computadora o conectarse externamente a un puerto USB, IEEE 1394 (FireWire), eSATA o eSATAp. Las capacidades de los discos duros se extienden hasta los terabytes. Los discos duros se actualizan con frecuencia en las computadoras, por lo que es importante que entiendas todas las cuestiones técnicas, incluido el reconocimiento de las partes del subsistema de disco duro, cómo trabajan juntos el sistema operativo y la BIOS/UEFI con un disco duro, y cómo configurar y solucionar problemas de un disco duro.

Los discos duros vienen en diferentes tamaños físicos (factores de forma). Para modelos de escritorio y servidores pequeños, hay disponibles unidades de 5.25 pulgadas (no muy populares) y 3.5 pulgadas. El factor de forma de 2.5 pulgadas está diseñado para computadoras portátiles. Hay disponible un factor de forma de 1.8 pulgadas y se puede encontrar para unidades de estado sólido (SSD), tabletas y dispositivos portátiles. La Figura 7.3 muestra dos tamaños de disco duro.

> Figura 7.3 Factores de forma de discos duros de escritorio

Un disco duro también se puede colocar dentro de una caja externa y conectarse mediante un puerto USB, eSATA, eSATAp combo o FireWire. La Figura 7.4 muestra una caja de disco duro Sabrent de PATA IDE o SATA a USB o eSATA que incluye un ventilador de refrigeración. Observa que el ventilador de refrigeración tiene un filtro que protege el ventilador de las partículas de polvo.

> Figura 7.4 Caja externa de disco duro Sabrent

### Geometría del disco duro magnético

Los discos duros mecánicos tradicionales son discos duros magnéticos. Estos discos duros tienen múltiples superficies metálicas duras llamadas platos. Cada plato normalmente contiene datos en ambas caras y tiene dos cabezales de lectura/escritura: uno para la cara superior y otro para la inferior. Los cabezales de lectura/escritura flotan sobre un colchón de aire sin tocar la superficie del plato. Los datos se escriben usando electromagnetismo. Se aplica una carga al cabezal de lectura/escritura, creando un campo magnético. El plato metálico del disco duro tiene partículas magnéticas que se ven afectadas por el campo magnético del cabezal de lectura/escritura, lo que permite «colocar» o «inducir» 1 y 0 en la unidad. La Figura 7.5 muestra los componentes principales dentro de un disco duro mecánico.

> Figura 7.5 Geometría del disco duro

Un disco duro magnético normalmente tiene dos motores: uno para hacer girar los platos y otro para mover los cabezales de lectura/escritura. Un disco duro gira a diferentes velocidades de rotación llamadas revoluciones por minuto (RPM). Las velocidades comunes son 5,400 RPM, 7,200 RPM, 10,000 RPM y 15,000 RPM. Cuanto mayor es el número de RPM de la unidad, más rápida es la velocidad de transferencia y, en general, mayor es el costo.

Si un cabezal de lectura/escritura toca el plato, se produce un choque de cabezal (head crash). Esto a veces se llama HDI (interferencia cabezal-disco, head-to-disk interference) y puede dañar los platos o el cabezal de lectura/escritura, causando corrupción de datos. Otro concepto importante es el tiempo medio entre fallos (MTBF): el número promedio de horas antes de que es probable que falle una unidad. Los discos duros mecánicos fallan, y por eso es tan importante respaldar los datos almacenados en ellos. La Figura 7.6 muestra el interior de un disco duro. Puedes ver el cabezal de lectura/escritura superior y los platos. Ten en cuenta que no debes quitar la cubierta de un disco duro, porque al hacerlo podrías permitir que entren partículas en el área sellada de la unidad.

> Figura 7.6 Disco duro con la cubierta quitada

La superficie del disco duro magnético es metálica y tiene círculos concéntricos, cada uno de los cuales se llama pista (track). Las pistas se numeran comenzando por la pista más externa, que se llama pista 0. Una pista correspondiente en todas las superficies de un disco duro es un cilindro. La Figura 7.7 muestra la diferencia entre pistas y cilindros. Cada pista se divide además en sectores. Normalmente, cada sector almacena 512 bytes.

> Figura 7.7 Cilindros, pistas y sectores

## Descripción general de la unidad de estado sólido (SSD)

Las SSD son dispositivos de almacenamiento que utilizan tecnologías de memoria flash no volátil en lugar de las tecnologías tradicionales de discos duros mecánicos. Las SSD eliminan la causa número uno de fallo de los discos duros: las partes móviles. Las SSD producen poco calor y son confiables, silenciosas, seguras, duraderas y rápidas. Las SSD se instalan en computadoras portátiles y modelos de escritorio como unidades internas y externas. Las SSD son comunes en tabletas y algunos dispositivos móviles. También se usan en entornos como temperaturas extremas o donde una unidad podría recibir sacudidas. Las SSD pueden usarse junto con el almacenamiento de discos duros mecánicos.

### Consejo técnico: no uses una SSD para almacenamiento de archivo

Las SSD pierden lentamente su carga si se dejan durante mucho tiempo sin alimentación.

El principal inconveniente de las SSD es el costo. Las SSD son caras en comparación con los discos duros mecánicos. Al igual que con las unidades flash, cada bloque de memoria de una SSD tiene un número finito de lecturas y escrituras. Una SSD que escribe datos en toda su capacidad de memoria durará más. Algunas empresas incluyen software con la unidad que ayuda con la instalación, la configuración, el rendimiento y la monitorización, y que rastrea o estima el fin de la vida útil. La Figura 7.8 muestra el interior de una SSD.

> Figura 7.8 Unidad de estado sólido sin cubierta

Hoy en día, hay disponibles SSD híbridas. Una SSD híbrida, o unidad híbrida de estado sólido (SSHD), ofrece una combinación de tecnologías mecánica y flash. La SSHD tiene algo de memoria flash integrada con una unidad mecánica tradicional (ver la Figura 7.9).

> Figura 7.9 SSHD

La memoria flash de una SSHD normalmente contiene los datos usados con más frecuencia que se enviarían a la interfaz del host. Se usan algoritmos avanzados para predecir estos datos. Solo si los datos solicitados no están en la memoria flash, los datos se extraerán de la unidad mecánica más lenta. Las SSHD ofrecen lo mejor de ambos mundos: los costos son más bajos por byte porque tienes un poco de almacenamiento de memoria realmente rápido gracias a la SSD, y hay mucho espacio de almacenamiento gracias a la unidad mecánica tradicional. Además, no necesitas una unidad tradicional de mayor RPM con una SSHD.

## Descripción general de las interfaces de unidades mecánicas

Un sistema de disco duro debe usar un conjunto de reglas para funcionar. Estas reglas conforman un estándar llamado interfaz que rige la comunicación con el disco duro. Hay dos interfaces principales de disco duro: Integrated Drive Electronics (IDE) —también conocida como el estándar AT Attachment (ATA) o Enhanced IDE (EIDE)— y Small Computer System Interface (SCSI). IDE es la más común en computadoras domésticas y de oficina. SCSI se encuentra más comúnmente en redes de almacenamiento o se usa con servidores de red.

Ten en cuenta que también se pueden usar otras interfaces para conectar dispositivos de almacenamiento externos. Casi todo el mundo ha visto una unidad flash o un disco duro externo conectado a un puerto USB. Este capítulo se centra más en las interfaces de almacenamiento internas.

Tanto IDE como SCSI empezaron como arquitecturas en paralelo, en las que se envían varios bits por múltiples rutas. Tal arquitectura requiere una sincronización precisa a medida que aumentan las velocidades de transferencia. Con IDE y SCSI, varios dispositivos pueden conectarse al mismo bus. Mientras que IDE en paralelo, o Parallel ATA (PATA), admite solo dos dispositivos, SCSI en paralelo admite más. Cuando varios dispositivos comparten el mismo bus, tienen que esperar su turno para acceder al bus, y hay problemas de configuración con los que lidiar.

En contraste, una arquitectura en serie es un bus punto a punto en el que cada dispositivo tiene una sola conexión de vuelta al controlador. Los bits se envían de uno en uno por un único enlace. Se pueden conectar más dispositivos a este tipo de arquitectura porque escala fácilmente y es fácil de configurar. La Figura 7.10 muestra el concepto de transferencias en paralelo y en serie.

> Figura 7.10 Transferencias de datos en paralelo vs. en serie

Hoy en día se usan arquitecturas en serie. Tanto el estándar IDE como el SCSI tienen disponibles arquitecturas en serie. El estándar ATA en serie se conoce como Serial ATA (SATA), y el estándar SCSI en serie se conoce como Serial Attached SCSI (SAS). Las unidades SATA se usan con computadoras portátiles y PC.

Tanto las unidades SATA como las SAS se usan con dispositivos de almacenamiento conectado a la red (NAS), servidores y redes de área de almacenamiento (SAN). Una unidad NAS funciona a velocidades de RPM más altas, almacena datos para uno o más servidores y/o computadoras, y está diseñada para funcionar 24/7 con un rendimiento optimizado. La Figura 7.11 muestra unidades SAS usadas en un centro de datos.

> Figura 7.11 Unidades SAS

### M.2 y NVMe

SATA en las computadoras portátiles está siendo reemplazado por una interfaz conocida como M.2. Una ranura M.2 permite conectar SSD y módulos Wi-Fi/Bluetooth de distintos tamaños. Una ranura M.2 puede interconectarse con SATA 3.0 y superior, PCIe 3.0 y superior, y USB 3.0 y superior. Ten en cuenta que actualmente una sola ranura M.2 puede usar un máximo de cuatro carriles PCIe y podría usar menos. Consulta la documentación de la placa madre para conocer las especificaciones exactas.

Los tamaños de tarjeta comunes incluyen 2242, 2260, 2280 y 22110. En estos tamaños, 22 se refiere al ancho, en milímetros, y los siguientes dos o tres números se refieren a la longitud. La documentación del dispositivo o de la placa madre indica qué tamaños se aceptan.

Los dispositivos M.2 también están codificados con muescas (keyed), lo que significa que hay separaciones entre los conectores dorados. Las tres muescas más comunes usadas son B, M y B+M. Un módulo que usa la muesca B usa hasta dos carriles PCIe, y la muesca M usa hasta cuatro carriles PCIe. La Figura 7.12 muestra cuatro tamaños de tarjetas M.2, una de ellas con una muesca M y las otras con la muesca B+M.

> Figura 7.12 Tamaños y muescas de SSD M.2

### Consejo técnico: las SSD con muesca B+M caben en ranuras B o M

Cualquier SSD con muesca B+M puede caber en un zócalo con muesca B o en un zócalo con muesca M.

Las SSD también pueden usar Non-Volatile Memory Express (NVMe), que ofrece un rendimiento más rápido al acceder a la memoria flash de las SSD. Las SSD funcionan mejor cuando se conectan al estándar NVMe de cuatro carriles PCIe. Para usar NVMe, una SSD normalmente se monta en una tarjeta PCIe o se conecta mediante un conector M.2 (ver la Figura 7.13). Asegúrate de que la placa madre admita una SSD NVMe antes de comprar e instalar una.

> Figura 7.13 SSD NVMe y no NVMe

### Conectividad PATA, SATA y SAS

PATA usa un cable IDE de 40 pines que conecta el disco duro a un adaptador o a la placa madre y transfiere 16 bits de datos a la vez. El conector SATA tiene siete conductores (cuatro líneas usadas para datos en pares de dos). La Figura 7.14 muestra tanto un cable IDE PATA como un cable SATA.

> Figura 7.14 Cables de datos SATA y PATA

Cada conector PATA de la placa madre permite conectar dos dispositivos a través del cable IDE. Un conector SATA se conecta a un solo dispositivo. La Figura 7.15 muestra la diferencia entre los conectores PATA y SATA de la placa madre.

> Figura 7.15 Conectores PATA y SATA de la placa madre

La especificación SATA original transfiere datos a 1.5 Gb/s y se llama SATA 1 o SATA I. La versión de 3 Gb/s se conoce como SATA 2 o SATA II, y la última versión, SATA 3 o SATA III, funciona a un máximo de 6 Gb/s. Estos dispositivos suelen verse marcados como SATA 1.5 Gb/s, 3 Gb/s y 6 Gb/s.

SATA es una interfaz punto a punto, lo que significa que cada dispositivo se conecta al host mediante un enlace dedicado, y cada dispositivo tiene el ancho de banda de toda la interfaz. SATA admite dispositivos tanto internos como externos. La Figura 7.16 muestra una unidad SATA interna con el cable conectado. El conector de datos y el cable están a la izquierda del conector de alimentación (que no tiene un cable de alimentación conectado).

> Figura 7.16 Disco duro SATA y cable de datos

Las placas madre de escritorio, las computadoras portátiles y los dispositivos móviles pueden hacer uso de un conector mSATA para la instalación de una SSD. Mientras que el factor de forma M.2 puede hacer uso de SATA o PCIe, el estándar mSATA solo permite el uso del estándar SATA. La Figura 7.17 muestra una SSD mSATA instalada.

> Figura 7.17 SSD mSATA y conector

Un dispositivo SATA interno normalmente usa un conector de alimentación SATA de 15 pines en lugar del conector Molex que usan los discos duros más antiguos. Sin embargo, algunas unidades se envían con conectores Molex. Se puede comprar un convertidor de Molex a SATA. La Figura 7.18 muestra un conector de alimentación Molex más antiguo y un conector de alimentación SATA interno.

> Figura 7.18 Conectores de alimentación de disco duro

Los cables de datos SATA internos están limitados a un máximo de 3.3 pies (1 metro). Es más probable que un cable de datos SATA interno se desenchufe sin querer, o se desenchufe parcialmente, que un cable PATA. Existen cables especiales con mecanismos de bloqueo en forma de L para lugares de difícil acceso, y también se pueden comprar cajas de perfil bajo. La Figura 7.19 muestra estos cables de dispositivo SATA internos de 7 pines.

> Figura 7.19 Cables de datos SATA internos

External SATA (eSATA) proporciona conectividad para dispositivos externos. Permite longitudes de cable blindado de hasta 6.56 pies (2 metros), con conexiones más rápidas que USB 2.0 o 3.0. Sin embargo, la conexión eSATA estándar no proporciona alimentación a los dispositivos externos, pero un puerto eSATAp combo (USB y eSATA) sí puede proporcionar alimentación. Ten en cuenta que eSATA actualmente no es más rápido que USB 3.1 gen 2. La Figura 7.20 muestra un cable eSATA y un puerto eSATA. Un cable eSATA puede tener una clasificación de 1.5 Gb/s, 3 Gb/s o 6 Gb/s. Los cables eSATA están limitados a 3.3 pies (1 metro) para dispositivos de 1.5 Gb/s y a 6.56 pies (2 metros) para transferencias de 3 Gb/s o 6 Gb/s.

> Figura 7.20 Puerto y cable eSATA

Hay varios conectores para unidades SCSI, pero el que los técnicos de PC ven con más frecuencia es el conector SCSI para una unidad Serial-Attached SCSI (SAS). El conector SAS se parece a los conectores de una unidad SATA, como se muestra en la Figura 7.21.

> Figura 7.21 Conector Serial-Attached SCSI (SAS)

Un cable Serial-Attached SCSI, o cable SAS, se usa para conectar discos duros o unidades de cinta a un controlador SAS. El cable que se muestra en la Figura 7.22 se usa para conectar un disco duro SAS a un controlador SATA que admite unidades SAS. Un solo cable proporciona tanto las conexiones de alimentación como las de datos.

> Figura 7.22 Cable SAS (Serial-Attached SCSI)

## Descripción general de la configuración de dispositivos de almacenamiento

La configuración de la unidad a veces incluye el ajuste de puentes (jumpers) en la unidad. Sin embargo, los fabricantes individuales de unidades pueden desarrollar sus propios pasos de configuración. Consulta la documentación incluida con la unidad, el adaptador o la placa madre para obtener información de configuración e instalación. Los pasos generales para instalar un dispositivo de almacenamiento son los siguientes:

Paso 1. Mantén la unidad en el contenedor antiestático protector hasta que estés listo para la instalación. Luego usa procedimientos de manejo antiestático adecuados al instalar la unidad y manipúlala por los bordes; evita tocar la electrónica y los conectores de la unidad.

Paso 2. Apaga la computadora y quita el cable de alimentación de la computadora antes de instalar la unidad.

Paso 3. Monta y fija físicamente el dispositivo en la computadora y conecta el cable adecuado.

Paso 4. Vuelve a conectar el cable de alimentación y enciende la computadora. Configura la BIOS/UEFI, si es necesario.

Paso 5. Si se está instalando un disco duro, prepara la unidad para los datos, como se describe más adelante en este capítulo.

### Instalación física de PATA

Un cable PATA permite conectar dos dispositivos de almacenamiento a un solo conector de la placa madre. Los dispositivos PATA se configuran mediante puentes. La opción más común usada es la selección de cable (cable select). Cuando se usa un solo dispositivo, ajusta el puente a selección de cable y conéctalo al conector negro que está en el extremo. Conecta el conector azul a la placa madre. Si se van a usar dos dispositivos, ajusta el puente de cada dispositivo a selección de cable. La Figura 7.23 ilustra cómo se conectan varios dispositivos PATA a la placa madre.

> Nota: El uso de los términos maestro y esclavo (master y slave) se hace SOLO en asociación con la terminología oficial usada en las especificaciones y estándares de la industria y de ninguna manera disminuye el compromiso de Pearson de promover la diversidad, la equidad y la inclusión, y de desafiar, contrarrestar y/o combatir los prejuicios y los estereotipos en la población global de estudiantes a quienes servimos.

> Figura 7.23 Dos dispositivos PATA configurados con selección de cable

### Instalación física de SATA

Las unidades SATA son fáciles de instalar. Un conector de datos de 7 pines se conecta desde la placa madre o la tarjeta SATA a la unidad SATA interna. Un cable de 15 pines conecta la alimentación a la unidad. El conector de alimentación SATA interno es exclusivo, pero posiblemente podría ser un conector Molex más antiguo. Se puede obtener un convertidor de cable si un conector Molex es el único disponible en la fuente de alimentación. La Figura 7.24 muestra cómo se conectan los cables a una unidad SATA interna. La Figura 7.25 muestra cómo se conectan dos unidades SATA a una placa madre que tiene dos conectores SATA.

> Figura 7.24 Cableado de datos (izquierda) y alimentación (derecha) SATA

> Figura 7.25 Conectividad SATA

La Figura 7.26 muestra un adaptador SATA que tiene dos puertos internos en el extremo más alejado y un puerto eSATA. Para instalar un adaptador host SATA, apaga la computadora y quita el cable de alimentación. Quita la cubierta de la computadora y localiza una ranura de expansión libre. Algunos adaptadores tienen puentes para opciones configurables. Para la mayoría de los adaptadores, la configuración predeterminada funcionará, pero consulta la documentación del adaptador para obtener más detalles.

> Figura 7.26 Tarjeta eSATA

### Consejo técnico: habilitar un puerto SATA en la BIOS/UEFI

Algunos fabricantes requieren que habilites el puerto de la placa madre a través de la BIOS/UEFI del sistema antes de que se reconozca cualquier dispositivo conectado al puerto.

Para instalar un disco duro SATA interno, apaga la computadora y quita el cable de alimentación de la computadora. Monta físicamente la unidad en una bahía de unidades. Ten en cuenta que es posible que tengas que instalar rieles en el costado de la unidad para deslizarla dentro de la carcasa, o fijar tornillos a la carcasa y al disco duro para montar la unidad, como se muestra en la Figura 7.27.

> Figura 7.27 Disco duro SATA instalado

Para añadir un módulo mSATA, apaga la computadora, quita la cubierta y localiza el conector mSATA de la placa madre. Inserta la tarjeta en el conector y fija los tornillos en el extremo opuesto, como se muestra en la Figura 7.28. Enciende la computadora y asegúrate de que la BIOS/UEFI lo reconoce.

> Figura 7.28 Instalación de mSATA

Una unidad externa (eSATA) normalmente no tiene puentes, terminadores ni interruptores que configurar. Sin embargo, al conectar una unidad más rápida a un puerto más lento —como cuando se instala una unidad de 3.0 Gb/s en un puerto de 1.5 Gb/s— es posible que haya que configurar un puente para que la unidad sea compatible con el puerto. Consulta la documentación del fabricante de la unidad al instalar una unidad. Conecta el cable de alimentación a la unidad, si corresponde, e inserta el otro extremo del cable de alimentación en un tomacorriente de pared. Conecta un extremo del cable eSATA a la unidad. Enchufa el otro extremo del cable en un puerto eSATA de la computadora. La Figura 7.29 muestra un disco duro externo que admite IEEE 1394 (FireWire), eSATA y USB, como puedes ver por los puertos en la parte posterior de la unidad.

> Figura 7.29 Disco duro externo

Antes de encender la alimentación de la unidad eSATA, asegúrate de que la unidad esté colocada donde permanecerá durante el funcionamiento y de que todos los cables de datos y alimentación estén bien conectados. Enciende la alimentación de la unidad. La unidad se monta. Cuando se monta una unidad, se abre un canal de comunicación entre la unidad y el sistema operativo. Siempre que se vaya a desconectar la unidad, debe desmontarse. Usa la herramienta Administración de discos de Windows para asegurarte de que la unidad es reconocida. La herramienta Administración de discos se trata más adelante en este capítulo.

### Consejo técnico: desmontar una unidad eSATA

Para desmontar una unidad eSATA, haz clic en el icono Quitar hardware de forma segura en el área de notificación y selecciona la letra de unidad adecuada. Quita la unidad cuando el sistema operativo te lo indique. Si no puedes encontrar este icono en Windows 10, usa el Explorador de archivos para localizar la unidad, haz clic derecho en ella y selecciona Expulsar.

### Instalación física de SSD

Para una computadora de escritorio, una SSD se puede instalar usando varios métodos que se pueden combinar:

- Montada internamente y conectada a un puerto SATA (o incluso PATA) de la placa madre e instalada igual que cualquier otro dispositivo SATA
- Insertada en un conector mSATA, como se describió anteriormente
- Como módulo NVMe en una tarjeta PCIe o insertado en una ranura M.2
- Como módulo SSD SATA insertado en una ranura M.2
- Como dispositivo externo conectado a un puerto eSATA, eSATAp o USB

La Figura 7.30 muestra una SSD interna que se conecta a un puerto SATA y que está montada en una ranura de unidad. La Figura 7.31 muestra un módulo NVMe insertándose en una ranura M.2. Asegúrate de que la computadora esté apagada y presiona el módulo firmemente dentro de la ranura. Normalmente, se necesita un tornillo para fijar el extremo más alejado del módulo.

> Figura 7.30 SSD SATA interna

> Figura 7.31 SSD NVMe interna en una ranura M.2

Las SSD normalmente no requieren controladores especiales. Consulta las instrucciones de montaje de la SSD proporcionadas por el fabricante. Los siguientes pasos son genéricos:

Paso 1. Apaga la computadora, quita el cable de alimentación y localiza una bahía de unidades vacía, un conector mSATA, un conector M.2 o una ranura de expansión PCIe, según el tipo de SSD que estés instalando. Si es SATA, asegúrate de que haya un conector de alimentación disponible.

Paso 2. Usa procedimientos antiestáticos adecuados. Si la instalas en una bahía de unidades, fija soportes de montaje a la SSD, que pueden tener que comprarse por separado, pueden venir con la unidad o pueden venir con la computadora.

Paso 3. Desliza la SSD dentro de la bahía de unidades, el conector o la ranura de expansión y fíjala, si es necesario.

Paso 4. Si se está instalando una unidad SATA, conecta el cable de datos desde la placa madre o el adaptador a la unidad y conecta un conector de alimentación.

Paso 5. Vuelve a instalar la cubierta de la computadora, vuelve a conectar el cable de alimentación y enciende la computadora.

Paso 6. Asegúrate de que la BIOS/UEFI reconoce la unidad.

### Consejo técnico: cuidado con la electricidad estática

Las SSD son memoria flash y son susceptibles a la electricidad estática. Usa procedimientos adecuados de manejo de ESD al instalar una SSD.

Si vas a instalar una SSD externa, usa los siguientes pasos:

Paso 1. Conecta el cable USB o eSATA adecuado desde la unidad a la computadora.

Paso 2. Enciende la SSD. El sistema debería reconocer la nueva unidad.

### Consejo técnico: ¿quieres actualizar una SSD con otra SSD?

Al actualizar una SSD que ya tiene el sistema operativo instalado, necesitas algo de espacio en la SSD original para clonar (copiar) la unidad y algún software de clonación que puede venir con la nueva unidad. Durante el proceso, es posible que debas asegurarte de que el software sepa que se está usando una unidad SSD. Si el proceso de clonación no va bien, es posible que debas iniciar desde una unidad flash Linux y usar GParted para eliminar las secciones de la unidad antes de intentar el proceso de nuevo. Considera clonar la unidad y luego cambiar el tamaño de la partición.

## Configuración del BIOS/UEFI del sistema para dispositivos de almacenamiento

Un disco duro se configura a través del programa de configuración de la BIOS/UEFI del sistema. Se accede a la configuración mediante pulsaciones de teclas durante el proceso de arranque. En las computadoras actuales, la BIOS/UEFI detecta automáticamente el tipo de disco duro. La información del tipo de unidad se guarda en la CMOS.

### Consejo técnico: configura la BIOS/UEFI según las instrucciones del fabricante de la unidad

Los fabricantes de unidades normalmente incluyen documentación que describe cómo configurar la unidad en la configuración de la BIOS/UEFI. Además, proporcionan software para cualquier sistema que no reconozca la unidad.

Los discos duros normalmente se configuran usando la función de detección automática (auto-detect), que determina automáticamente el tipo de unidad para el sistema. La Tabla 7.1 muestra la configuración de dispositivos de almacenamiento más comúnmente usada. Las unidades SATA se pueden configurar en diferentes modos de funcionamiento:

- Modo heredado (Legacy): este modo se usa en un sistema que no tiene controladores SATA de forma nativa.
- Modo Advanced Host Controller Interface (AHCI): cuando está habilitado, el modo AHCI permite insertar/quitar unidades SATA con la alimentación encendida y te permite usar comandos para que los circuitos host se comuniquen con los dispositivos conectados a fin de implementar funciones SATA avanzadas.
- Modo RAID: RAID se trata más adelante en este capítulo.

Ten en cuenta que la BIOS/UEFI también es donde se selecciona la unidad que arrancará el sistema.

**Tabla 7.1 Configuración común de dispositivos de almacenamiento en la BIOS/UEFI**

| Tipo de dispositivo | Configuración de BIOS/UEFI |
| --- | --- |
| IDE<br>PATA/SATA/SCSI/SAS | AUTO |
| SATA | Modo SATA: modo IDE (sin AHCI ni RAID) |
| SATA | Modo SATA: SATA o AHCI (AHCI habilitado) |
| SATA | Modo SATA: RAID (AHCI y RAID habilitados) |
| mSATA | AUTO |
| NVMe SSD | Es posible que tengas que configurar el ancho de banda de PCIe a x2 o x4 |
| M.2 SSD | Es posible que tengas que habilitarlo; es posible que tengas que ir a una ranura PCIe específica y configurar el modo a M.2 |

Es importante asegurarse de que la BIOS/UEFI reconoce un dispositivo antes de prepararlo para aceptar datos o de intentar que el dispositivo almacene datos. Sin importar el tipo de dispositivo de almacenamiento, entra en la BIOS/UEFI y asegúrate de que el dispositivo sea reconocido y esté configurado según sea necesario. Es posible que tengas que usar la configuración avanzada para acceder a las opciones del dispositivo de almacenamiento.

## Descripción general de la preparación del disco duro

Después de instalar y configurar correctamente un disco duro y de que el tipo de disco duro sea reconocido y se vea dentro del programa de configuración, la unidad debe prepararse para aceptar datos. Los dos pasos de la preparación de un disco duro son los siguientes:

Paso 1. Particionar la unidad.

Paso 2. Realizar un formato de alto nivel en el disco duro.

### Consejo técnico: formato de bajo nivel

El formato de bajo nivel puede realizarse en la fábrica del disco duro. Algunos fabricantes proporcionan software que te permite hacer un formato de bajo nivel en la unidad, pero solo debes hacerlo bajo la dirección del fabricante.

Particionar un disco duro implica permitir que se asigne una letra de unidad a una o más secciones del disco duro. El formato de alto nivel implica preparar la unidad para su uso con un sistema de archivos en particular y permite que la unidad acepte datos del sistema operativo. Una unidad no puede usarse hasta que haya sido particionada y se le haya hecho el formato de alto nivel; por lo tanto, los técnicos deben estar muy familiarizados con estos pasos.

### Particionado

Como se acaba de mencionar, el primer paso para preparar un disco duro para su uso es el particionado. Particionar un disco duro significa dividir la unidad en secciones separadas para que el sistema informático vea el disco duro como más de una unidad. Cada sección de la unidad recibe una letra de unidad. La Figura 7.32 muestra un plato de disco duro con algunas secciones de color. Cada sección entre las líneas de color puede ser un volumen y puede recibir una letra de unidad diferente.

> Figura 7.32 Visualización del particionado

El particionado puede hacerse durante el proceso de instalación de Windows o usando el programa Administración de discos de Windows. De manera similar, la utilidad diskpart puede usarse desde el símbolo del sistema. La Administración de discos normalmente se usa para particionar discos duros adicionales y para administrarlos todos. El primer disco duro de un sistema normalmente se particiona como parte del proceso de instalación de Windows. Se pueden crear particiones adicionales usando la Administración de discos después de instalar el sistema operativo.

El particionado proporciona ventajas como las siguientes:

- Dividir un disco duro en subunidades separadas a las que luego el sistema operativo asigna letras de unidad, como C: o D:
- Organizar el disco duro para separar múltiples sistemas operativos, aplicaciones y datos
- Proporcionar seguridad de los datos colocándolos en una partición diferente para facilitar el respaldo, así como la protección
- Usar el disco duro a su máxima capacidad

### Consejo técnico: cómo determinar qué sistema de archivos se está usando

Haz clic derecho en cualquier unidad del Explorador de Windows (Windows 7) o del Explorador de archivos (Windows 8/10) y selecciona Propiedades. La pestaña General muestra el tipo de sistema de archivos que se está usando.

El propósito original del particionado era hacer posible cargar múltiples sistemas operativos. Hoy en día, esta sigue siendo una buena razón porque colocar cada sistema operativo en su propia partición elimina los errores y los dolores de cabeza causados por múltiples sistemas operativos y múltiples aplicaciones que coexisten en la misma partición. El tipo de partición y el tamaño que puede tener dependen del sistema de archivos que se use. Un *sistema de archivos* (file system) define cómo se almacenan los datos en una unidad. Los sistemas de archivos de Windows más comunes son FAT16, FAT32, exFAT y NTFS. Qué sistema de archivos se puede usar depende del sistema operativo instalado, de si el dispositivo es interno o externo y de si se van a compartir archivos. La Tabla 7.2 enumera los sistemas de archivos y explica un poco sobre cada uno.

**Tabla 7.2 Sistemas de archivos**

| Sistema de archivos | Descripción |
| --- | --- |
| FAT | También llamado FAT16. Se usa con todas las versiones de Windows. Limitación de partición de 2 GB con sistemas operativos antiguos. Limitación de partición de 4 GB con XP y versiones superiores de Windows. |
| FAT32 | Compatible con todas las versiones de Windows. Se usa comúnmente con unidades flash extraíbles. Admite unidades de hasta 2 TB. Puede reconocer volúmenes mayores de 32 GB, pero no puede crearlos de ese tamaño. |
| exFAT | Comúnmente llamado FAT64. Un sistema de archivos hecho para medios extraíbles (como unidades flash y tarjetas SD) que amplía el soporte del tamaño de unidad hasta 64 ZB en teoría, pero 512 TB es el máximo recomendado. Está hecho para copiar archivos grandes como imágenes de disco y archivos multimedia. Compatible con todas las versiones de Windows. |
| NTFS | Se usa con Windows 7, 8 y 10. Admite unidades de hasta 16 EB (16 exabytes, que equivale a 16 mil millones de gigabytes), pero en la práctica solo 16 TB. Admite compresión de archivos y seguridad de archivos (cifrado). NTFS permite un acceso más rápido a los archivos y usa el espacio del disco duro de forma más eficiente en comparación con FAT (FAT16) y FAT32. Admite compresión de archivos individuales y tiene la mejor seguridad de archivos. |
| Apple File System (APFS) | Propiedad de Apple, diseñado teniendo en mente el cifrado y funciona en todas las plataformas de Apple. Usa particiones GPT, que se tratan más adelante en este capítulo, y permite la clonación de discos. |
| ext3 | También conocido como tercer sistema de archivos extendido. Se usa en sistemas operativos basados en Linux y es un sistema de archivos con registro (journaling), lo que significa que rastrea los cambios en caso de que el sistema operativo falle, lo que permite reiniciarlo sin recargarlo. |
| ext4 | Una actualización de ext3 que permite volúmenes y tamaños de archivo más grandes dentro de los sistemas operativos basados en Linux. |

Una razón aún mejor para particionar que cargar múltiples sistemas operativos o separar el sistema operativo de los datos es particionar el disco duro para un uso más eficiente del espacio. Un sistema operativo reserva al menos un clúster para cada archivo. Un *clúster* (cluster) es la menor cantidad de espacio reservada para un archivo, y está formado por un número específico de sectores. La Figura 7.33 ilustra el concepto de clúster. Ten en cuenta que el número de sectores por pista de un disco duro varía. Las pistas externas contienen más información (es decir, tienen más sectores) que las pistas internas.

> Figura 7.33 Clúster

### Consejo técnico: cómo convertir particiones

Usa el programa convert en Windows para convertir una partición FAT16, FAT32 o exFAT a NTFS sin pérdida de datos. Accede a una ventana de símbolo del sistema y escribe el comando `convert x: /fs:ntfs`, donde x es la letra de unidad de la partición que se va a convertir a NTFS. Pulsa <kbd>Enter</kbd> y luego pulsa <kbd>Y</kbd> y pulsa <kbd>Enter</kbd>. Puedes añadir un modificador /V al final del comando para un modo de operación más detallado (verbose).

Cualquier tipo de conversión de partición requiere espacio libre en el disco duro. La cantidad depende del tamaño de la partición. La Tabla 7.3 muestra que particionar unidades grandes en una sola partición FAT desperdicia espacio en la unidad. Un disco duro particionado de forma eficiente permite guardar más archivos porque se desperdicia menos espacio en el disco duro.

**Tabla 7.3 Ejemplos de particiones FAT16 y tamaños de clúster**

| Tamaño de partición | Número de sectores | Tamaño de clúster |
| --- | --- | --- |
| 0-32 MB | 1 | 512 bytes |
| 1 GB–2 GB | 64 | 32 kB |
| 2 GB–4 GB | 128 | 64 kB |

> Nota del traductor: la tabla original del libro es una imagen de baja resolución; se transcriben las filas legibles. Es una tabla de ejemplo (muestra), no exhaustiva.

Una buena práctica es colocar las aplicaciones en una partición separada de los archivos de datos. Las siguientes son algunas buenas razones para particionar un disco duro y separar los archivos de datos de los archivos de aplicación:

- Varias particiones en el mismo disco duro dividen la unidad en subunidades más pequeñas, lo que hace que sea más fácil y rápido respaldar los datos (que deberían respaldarse con más frecuencia que las aplicaciones).
- Los datos se protegen de fallos del sistema operativo, aplicaciones inestables y cualquier problema de software inusual que ocurra entre la aplicación y el sistema operativo.
- Los datos están en una sola ubicación, lo que hace que respaldar, organizar y localizar los archivos sea más fácil y rápido.

Las particiones FAT32 existen desde hace mucho tiempo y todavía se usan. Las unidades flash comúnmente se formatean en FAT32 debido a la «escritura diferida» (lazy write) de NTFS, que prolonga una escritura y podría no liberar una unidad externa durante algún tiempo. El sistema de archivos FAT32 hace un uso más eficiente del disco duro que FAT16. NTFS es un sistema de archivos eficiente. La Tabla 7.4 enumera los tamaños de clúster predeterminados para todas las versiones de Windows 7 y superiores.

**Tabla 7.4 Particiones y tamaños de clúster de NTFS**

| Tamaño de partición | Número de sectores | Tamaño de clúster |
| --- | --- | --- |
| 0-16 TB | 8 | 4 kB |
| 16 TB–32 TB | 16 | 8 kB |
| >32 TB–64 TB | 32 | 16 kB |
| >64 TB–128 TB | 64 | 32 kB |
| >128 TB–256 TB | 128 | 64 kB |

La Figura 7.34 muestra una captura de pantalla de la ventana Administración de discos de Windows 10 que tiene varias unidades (Disco 0, Disco 1, Disco 2) y varias particiones en el Disco 1 y el Disco 2.

> Figura 7.34 Herramienta Administración de discos de Windows 7

### Consejo técnico: beneficios de NTFS

NTFS admite cuotas de disco, lo que significa que los usuarios individuales pueden estar limitados en la cantidad máxima de espacio utilizable del disco duro. NTFS también puede reparar automáticamente los problemas del disco. Por ejemplo, cuando un sector del disco duro se está degradando, NTFS mueve todo el clúster a otro clúster.

Las particiones se definen como primarias y extendidas. Si solo hay un disco duro instalado en un sistema y todo el disco duro es una sola partición, es la partición primaria. A la partición primaria del primer disco duro detectado se le asigna la letra de unidad C:.

### Consejo técnico: las eSATA ya están particionadas

La mayoría de las unidades eSATA ya están particionadas y formateadas, pero estas unidades se pueden reparticionar y reformatear según sea necesario mediante la herramienta Administración de discos.

Si se divide una unidad, solo parte de la unidad es la partición primaria. En sistemas operativos antiguos, el resto de los cilindros se pueden designar como particiones extendidas. Una partición extendida permite que una unidad se divida aún más en unidades lógicas. Una unidad lógica a veces se llama volumen. A un volumen se le asigna una letra de unidad y puede incluir una unidad lógica y medios extraíbles como un CD, DVD, BD o unidad flash. Solo puede haber una partición extendida por unidad. En sistemas operativos anteriores a Windows Vista, un solo disco duro podía dividirse en un máximo de cuatro particiones primarias. Recuerda que una partición es una sección contigua de espacio de almacenamiento que funciona como si fuera una unidad separada. La Figura 7.35 ilustra cómo se puede dividir un disco duro en particiones.

> Figura 7.35 Particionado de disco duro

El primer disco duro de un sistema informático debe tener una partición primaria, pero no se requiere una partición extendida. Si la unidad tiene una partición extendida, se puede subdividir o dividir en unidades lógicas que aparecen como discos duros separados para el sistema informático. A las unidades lógicas creadas en la partición extendida se les asignan letras de unidad como D: o E:. El único límite para las unidades lógicas es el número de letras de unidad. Un segundo sistema operativo puede residir en una unidad lógica. La Figura 7.36 ilustra un disco duro dividido en una partición primaria y una partición extendida que se subdivide además en dos unidades lógicas.

> Figura 7.36 Dos unidades lógicas

Si se instalan dos discos duros en una computadora, el primer disco duro debe tener una partición primaria. El segundo disco duro no está obligado a tener una partición primaria y puede simplemente tener una sola partición extendida. Si el segundo disco duro sí tiene una partición primaria, también puede tener una partición extendida. Hoy en día, pueden existir más de cuatro particiones primarias, y las secciones simplemente se llaman volúmenes.

Cuando un disco duro se instala y particiona por primera vez, la pista más externa del plato (cilindro 0, cabezal 0 y sector físico 1) se reserva para la tabla de particiones. La tabla de particiones contiene información sobre los tipos de particiones creadas y en qué cilindros residen esas particiones. La tabla de particiones es parte del registro de arranque maestro (MBR), que contiene un programa que lee la tabla de particiones, busca la partición primaria marcada como activa y va a esa partición para arrancar el sistema. La Figura 7.37 muestra las ubicaciones de partes importantes del disco duro que permiten arrancar, leer particiones y acceder a los archivos.

> Figura 7.37 Estructura del disco duro

NTFS tiene dos términos adicionales que debes conocer como técnico:

- Partición del sistema (System partition): la partición del disco duro que contiene los archivos específicos del hardware necesarios para cargar el sistema operativo.
- Partición de arranque (Boot partition): la partición del disco duro que contiene el sistema operativo.

En Windows, la partición de arranque y la partición del sistema pueden estar en la misma partición.

### Consejo técnico: ¿qué ocurre cuando se eliminan diferentes tipos de particiones?

Cuando se elimina una partición, se pierde toda la información de la partición. Cuando se eliminan unidades lógicas de una partición extendida, se pierden todos los datos. Las otras unidades lógicas dentro de la partición extendida conservan su información.

El Host Protected Area (HPA) es un área oculta de un disco duro que se usa para guardar una copia del sistema operativo; a veces las aplicaciones instaladas usan el HPA cuando el sistema operativo se corrompe tanto que es necesaria una reinstalación. Muchos fabricantes proporcionan una configuración de BIOS/UEFI o una pulsación de tecla que se puede usar cuando el sistema arranca para acceder a esta área.

La tabla de particiones GUID, o identificador único global (GPT), está disponible con sistemas operativos Windows de 64 bits. El particionado GPT se realiza usando la herramienta Administración de discos o la utilidad de línea de comandos diskpart. La Tabla 7.5 compara los discos MBR con los GPT.

**Tabla 7.5 Características de los discos MBR y GPT**

| Característica | MBR | GPT |
| --- | --- | --- |
| Tamaño de partición | Hasta 2 TB | Hasta 9.4 ZB |
| Tipos de particiones | Hasta 4 primarias; admite particiones extendidas | Hasta 128 primarias |
| Firmware | BIOS o UEFI | UEFI |
| Sistema operativo | Windows | Windows 7/8/10/11 de 64 bits o superior |
| Tabla de particiones | Una sola tabla de particiones | Tiene una tabla de particiones de respaldo |

### Consejo técnico: pierdes datos al convertir a GPT

Las particiones basadas en MBR se pueden convertir a GPT y viceversa, pero los datos no se conservan. Esto se ve solo en sistemas que tienen una BIOS UEFI. ¡Haz una copia de seguridad de los datos si conviertes!

Se pueden usar productos especiales para particionar un disco duro y también reparticionarlo sin pérdida de datos. Entre los ejemplos se incluyen Disk Director de Acronis, Partition Master de EaseUS y Partition Commander de Avanquest.

### Cómo se asignan las letras de unidad

Un sistema operativo asigna letras de unidad a los discos duros durante el paso de particionado. El orden en que se asignan las letras de unidad a las particiones depende de tres factores: el número de discos duros, el tipo de volumen de los discos duros (primario o extendido) y el sistema operativo.

Ten en cuenta que si se instala una nueva unidad, las letras de unidad de dispositivos, volúmenes, particiones o unidades lógicas se añaden después. Las letras de unidad se pueden cambiar a través de la herramienta Administración de discos o usando la utilidad de línea de comandos diskpart. Sin embargo, ten cuidado, porque algunas aplicaciones tienen punteros a archivos específicos en letras de unidad específicas.

### Formato de alto nivel

Como se mencionó anteriormente, el segundo paso para preparar un disco duro para su uso es el formato de alto nivel. El formato de alto nivel debe realizarse en todas las particiones primarias, las unidades lógicas ubicadas dentro de particiones extendidas y las particiones GPT antes de que se puedan escribir datos en el disco duro. El formato de alto nivel configura el sistema de archivos para que pueda aceptar datos.

NTFS permite la compatibilidad con múltiples flujos de datos, así como la compatibilidad con todos los caracteres del mundo. NTFS también reasigna automáticamente los clústeres defectuosos a otras secciones del disco duro sin tiempo ni utilidad adicionales. Durante el proceso de instalación, Windows permite un formato rápido (donde ves la palabra «(rápido)» después de la opción) o un formato completo (a veces llamado formato estándar). Un *formato completo* (full format) examina y marca los sectores defectuosos. Esto evita que el sistema operativo se instale en un sector que podría causar problemas al sistema operativo. Un *formato rápido* (quick format) simplemente prepara la unidad para los datos y lleva mucho menos tiempo que un formato completo. Usa un formato completo si sospechas que una unidad tiene problemas.

La Figura 7.38 muestra la estructura de la partición NTFS una vez que se ha configurado y se ha completado el formato de alto nivel.

> Figura 7.38 Estructura del volumen NTFS

El formato de alto nivel crea dos tablas de asignación de archivos (FAT): una primaria y una secundaria. El proceso de formato también crea el directorio raíz que renumera los sectores. La FAT realiza un seguimiento de las ubicaciones de los archivos en el disco duro. Es similar a una tabla de contenido de un libro, ya que enumera dónde se encuentran los archivos en la partición. La Tabla 7.6 muestra las diferencias entre los sistemas de archivos.

**Tabla 7.6 Comparación de los sistemas de archivos de Windows**

| Especificación | FAT16 | FAT32 | NTFS | exFAT |
| --- | --- | --- | --- | --- |
| Tamaño máximo de archivo | 4 GB | 4 GB | ~16 TB | ~16 EB |
| Tamaño máximo de volumen (partición) | 4 GB (2 GB, si se comparte con una computadora muy antigua) | 32 GB (formato máximo) | 2 TB (o mayor) | 64 ZB (se recomiendan 512 TB) |
| Máximo de archivos por volumen | ~64,000 | ~4 millones | ~4 mil millones | No definido (pero 1,000 por directorio) |

El formato de alto nivel se puede realizar usando el comando format o la herramienta Administración de discos de Windows. El área del disco que contiene información sobre los archivos del sistema, el registro de arranque de DOS (DBR), se encuentra en el cilindro 0, cabezal 1, sector 1 del disco duro. El término más común para esto hoy en día (porque DOS ya no es un sistema operativo importante) es sector de arranque (boot sector), o registro de arranque de volumen.

Las particiones y unidades adicionales instaladas después de crear la primera partición del disco duro usan la herramienta Administración de discos de Windows para aplicar el formato de alto nivel a la unidad. La primera partición del disco duro normalmente tiene el formato de alto nivel realizado como parte del proceso de instalación del sistema operativo.

### Administración de discos de Windows

En el entorno Windows, los dispositivos de almacenamiento se administran con la herramienta Administración de discos. En Windows, hay dos tipos de almacenamiento: almacenamiento básico y almacenamiento dinámico. La gran diferencia entre estos dos es que puedes hacer particiones y cambios de tamaño con un disco dinámico, pero no con un disco básico. La Tabla 7.7 explica estos y otros términos asociados. La Figura 7.39 muestra algunos de estos conceptos.

### Consejo técnico: la hibernación afecta el espacio en disco

Siempre que pones la computadora en modo de suspensión/hibernación, la información de la RAM se almacena temporalmente en el disco duro. Esto requiere espacio libre en el disco duro.

**Tabla 7.7 Términos de administración de discos lógicos**

| Término | Descripción |
| --- | --- |
| Almacenamiento básico (Basic storage) | Uno de los dos tipos de almacenamiento. Esto es lo que tradicionalmente se ha conocido como partición. Es el predeterminado que usan todos los sistemas operativos. |
| Disco básico (Basic disk) | Cualquier unidad que ha sido particionada y configurada para escribir archivos. Un disco básico tiene particiones primarias, particiones extendidas y unidades lógicas contenidas dentro de las particiones extendidas. |
| Almacenamiento dinámico (Dynamic storage) | El segundo tipo de almacenamiento; contrástalo con el almacenamiento básico. Te permite crear particiones primarias, unidades lógicas y volúmenes dinámicos en dispositivos de almacenamiento. Es más potente que el almacenamiento básico porque permite la creación de volúmenes simples, distribuidos o seccionados (striped) usando discos dinámicos. |
| Disco dinámico (Dynamic disk) | Un disco compuesto de volúmenes. Un volumen puede ser todo el disco duro, partes del disco duro combinadas en una unidad y otros tipos específicos de volúmenes, como volúmenes simples, distribuidos o seccionados. No puede estar en una unidad extraíble. |
| Volumen simple (Simple volume) | Espacio de disco asignado desde un solo disco duro. El espacio no tiene que ser contiguo. |
| Volumen distribuido (Spanned volume) | Espacio de disco creado a partir de múltiples discos duros. También conocido como «simplemente un montón de discos» (JBOD). Windows escribe datos en un volumen distribuido de manera que se usa el primer disco duro hasta que se llena su espacio. Luego, se usa el espacio del segundo disco duro para escribir. Esto continúa hasta que se utilizan todos los discos duros del volumen distribuido. |
| Volumen seccionado (Striped volume) | Espacio de disco en el que los datos se escriben a través de 2 a 32 discos duros. Es diferente de un volumen distribuido en que las unidades se usan alternativamente. Otro nombre para esto es seccionado (striping), o RAID 0 (que se trata en la siguiente sección). |
| Volumen del sistema (System volume) | Espacio de disco que contiene los archivos necesarios para iniciar el sistema operativo. |
| Volumen de arranque (Boot volume) | Espacio de disco que contiene el resto de los archivos del sistema operativo. Puede ser el mismo volumen que el volumen del sistema. |
| Volumen RAW (RAW volume) | Un volumen que nunca ha tenido formato de alto nivel y que no contiene un sistema de archivos. |

> Figura 7.39 Conceptos de Administración de discos

Un disco básico, un volumen simple o un volumen distribuido se pueden redimensionar, reducir o ampliar sin afectar los datos. Cuando trabajes dentro de Administración de discos, haz clic derecho en una unidad para ver todas las opciones disponibles, como ver las propiedades de la unidad, marcar una partición como activa, cambiar la letra de unidad y las rutas, formatear, extender un volumen, reducir un volumen, añadir un reflejo (mirror) o eliminar un volumen.

### Consejo técnico: administrar discos y particiones

Usa la herramienta Administración de discos (desde la consola Administración de equipos, o haciendo clic derecho en el botón Inicio en Windows 10 y seleccionando Administración de discos, o usando el comando `diskmgmt.msc`) para determinar qué tipo de partición tienes, para trabajar con discos dinámicos o para convertir un disco básico en uno dinámico. Este proceso de conversión no se puede revertir.

Para extender (hacer más grande), dividir (partir en dos secciones) o reducir (disminuir el tamaño de) una partición, usa los siguientes pasos:

Paso 1. Accede a la herramienta Administración de discos de Windows.

Paso 2. Haz clic derecho en el volumen de la unidad.

Paso 3. Selecciona Reducir volumen (Shrink Volume) o Extender volumen (Extend Volume).

La Figura 7.40 muestra una partición de disco duro y la configuración usada para reducirla de modo que se pueda crear otra partición.

> Figura 7.40 Redimensionar una partición

### Tolerancia a fallos

Con una matriz de unidades, se configuran dos o más discos duros para velocidad, redundancia o ambas cosas (ver la Figura 7.41). Redundant array of independent (or inexpensive) disks (RAID) permite leer y escribir en múltiples discos duros para obtener áreas de almacenamiento más grandes, mejor rendimiento y tolerancia a fallos. La tolerancia a fallos es la capacidad de seguir funcionando después de un fallo de hardware o software. Una matriz RAID se puede implementar con hardware o software. RAID por hardware se configura a través de la BIOS/UEFI.

> Figura 7.41 RAID

Los pasos genéricos para configurar RAID por hardware son los siguientes:

Paso 1. Asegúrate de que los puertos de la placa madre que quieres usar estén habilitados.

Paso 2. Asegúrate de tener los controladores RAID para los discos duros usados en el RAID.

Paso 3. Instala y cablea físicamente los discos duros.

Paso 4. Entra en la BIOS/UEFI y habilita RAID.

Paso 5. Configura RAID en la BIOS/UEFI o mediante una secuencia de teclas especial para entrar en la configuración de la BIOS RAID.

Paso 6. Instala Windows en un RAID usando la opción de instalación Personalizada (Avanzada).

RAID por software se configura a través de Windows o mediante el software proporcionado por el fabricante del adaptador RAID. Si quieres poder controlar RAID a través de Windows y redimensionar los volúmenes o hacer ajustes, usa RAID por software.

RAID también se puede implementar con módulos de caché flash (FCM) y un disco duro mecánico tradicional. El software del dispositivo host y/o los controladores de dispositivo proporcionan la optimización y la supervisión.

RAID viene en muchos niveles diferentes, pero los que se implementan en el entorno Windows son 0, 1 y 5. Los que están en el examen de certificación A+ son los niveles RAID 0, 1, 5 y 10. Algunas placas madre admiten RAID «anidado», en el que se combinan niveles de RAID. Este método también aumenta la complejidad de la configuración del disco duro. La Tabla 7.8 explica los niveles de RAID.

**Tabla 7.8 RAID**

| Nivel de RAID | Descripción |
| --- | --- |
| RAID 0 | También llamado seccionado de discos (disk striping) o seccionado de discos sin paridad. Los datos se escriben alternativamente en dos o más discos duros, lo que aumenta el rendimiento del sistema. El sistema ve estos discos como una sola unidad lógica. RAID 0 no protege los datos cuando un disco duro falla. No se considera tolerante a fallos. Tiene el rendimiento de lectura y escritura más rápido. |
| RAID 1 | También llamado duplicación de discos (disk mirroring) o duplexación de discos (disk duplexing). RAID 1 protege contra fallos de disco duro usando dos o más discos duros y un controlador de disco. Los mismos datos se escriben en dos discos, de modo que si un disco falla, el sistema sigue funcionando. La duplexación de discos es similar, excepto que se usan dos controladores de disco. Con la duplexación de discos, el rendimiento se degrada ligeramente al escribir datos porque hay que escribirlos en dos discos. |
| RAID 0+1 | Un conjunto seccionado y un conjunto duplicado combinados. Se requieren al menos cuatro discos duros, y deben tener un número par de discos. Un segundo conjunto seccionado duplica un conjunto seccionado primario de discos. También llamado RAID 01, este modo puede leer del disco rápidamente, pero hay una ligera degradación al escribir. |
| RAID 1+0 | Un conjunto duplicado y un conjunto seccionado combinados con al menos cuatro discos duros. La diferencia entre 1+0 y 0+1 es que 1+0 tiene un conjunto seccionado a partir de un conjunto de discos duplicados. Este modo, también llamado RAID 10, puede leer del disco rápidamente pero tiene una ligera degradación al escribir. |
| RAID 5 | También llamado seccionado de discos con paridad (disk striping with parity). RAID 5 escribe datos en tres o más discos duros. Junto con los datos se incluye información de paridad. Si un disco falla, los datos se pueden reconstruir basándose en la información de los otros dos discos. Este nivel puede leer y escribir datos rápidamente. |

La Figura 7.42 muestra los diferentes tipos de RAID. Con RAID 0, los bloques de datos (B1, B2, B3, etc.) se colocan en unidades alternas. Con RAID 1, el mismo bloque de datos se escribe en dos unidades. RAID 5 tiene una unidad que contiene información de paridad (P) para bloques particulares de datos, como B1 y B2.

> Figura 7.42 Conceptos de RAID

Windows 7 Professional y versiones superiores admiten volúmenes simples, distribuidos, seccionados y reflejados (mirrored). Ten en cuenta que un volumen distribuido no proporciona redundancia ni tolerancia a fallos, como sí lo hacen la mayoría de los niveles de RAID.

Las unidades RAID con frecuencia son de intercambio en caliente (hot swappable); es decir, se pueden quitar o instalar mientras la computadora está alimentada. USB, SATA y SAS admiten el intercambio en caliente, pero no es obligatorio que RAID lo admita. Consulta el manual de la unidad y de la computadora antes de intercambiar en caliente cualquier disco duro. Las reconstrucciones de RAID consumen mucho tiempo y muchas operaciones de entrada/salida (E/S). Prepárate para que el sistema esté fuera de servicio durante un tiempo; la cantidad de tiempo que el sistema estará no disponible depende del tamaño de la unidad y del tipo de RAID.

El RAID por hardware para una computadora doméstica o de empresa solía requerir un adaptador RAID independiente y software para realizar el RAID. Ahora muchas placas madre admiten RAID, y también lo hacen los sistemas operativos Windows 7 y superiores. Muchas veces, debes configurar la BIOS/UEFI de la placa madre para RAID como parte de tu configuración inicial. La Tabla 7.9 muestra algunos parámetros comunes de configuración de la BIOS RAID.

**Tabla 7.9 Configuración de la BIOS/UEFI de RAID**

| Configuración de BIOS/UEFI | Descripción |
| --- | --- |
| Modo SATA: modo AHCI | Un modo que puede significar que se admite el intercambio en caliente. Se puede usar un conjunto de comandos para aumentar el rendimiento del almacenamiento. |
| Modo SATA: modo RAID o modo SATA discreto | Permite seleccionar un nivel de RAID particular y las unidades asociadas con el RAID. |
| Unidades SATA: volumen RAID detectado | Generalmente una pantalla de información que muestra el tipo de RAID configurado, si lo hay. |
| Unidades SATA: modo de controlador eSATA | Permite la configuración de RAID a través del puerto eSATA. |
| Unidades SATA: capacidad de conexión en caliente del puerto eSATA x | Permite habilitar o deshabilitar el intercambio en caliente para los puertos eSATA. |

### Espacios de almacenamiento de Windows

Microsoft Windows 8 y Windows 10 admiten Espacios de almacenamiento de Windows (Windows Storage Spaces), que combina unidades en una opción de almacenamiento de datos flexible. Un administrador primero crea un grupo de almacenamiento (storage pool), que son dos o más discos físicos que pueden ser de diferentes tipos, como una unidad SATA y una unidad USB. Un espacio de almacenamiento (storage space) es un disco virtual creado a partir del espacio disponible en un grupo de almacenamiento. Hay tres tipos de espacios de almacenamiento:

- Simple: los datos se seccionan (striped) entre los discos físicos. No se proporciona resiliencia. Este tipo de espacio de almacenamiento proporciona el mayor rendimiento, pero hay pérdida de datos si falla un disco.
- Paridad (Parity): los datos se seccionan entre los discos físicos y se incluye información de paridad. Este tipo de espacio de almacenamiento ralentiza el rendimiento.
- Reflejo (Mirror): los datos se seccionan entre varios discos y se copian los mismos datos para obtener el mayor nivel de resiliencia.

A diferencia de RAID, si añades una unidad a un espacio de almacenamiento, los datos no se reescriben para incluir la nueva unidad. En su lugar, los nuevos datos usan todas las unidades. Para crear un espacio de almacenamiento, sigue estos pasos:

Paso 1. Accede al enlace Espacios de almacenamiento del Panel de control de Windows. Selecciona Crear un nuevo grupo y espacio de almacenamiento.

Paso 2. Selecciona las unidades que se van a usar y luego selecciona Crear grupo (ver la Figura 7.43).

> Figura 7.43 Espacios de almacenamiento de Windows: crear un grupo de almacenamiento

Paso 3. Asigna un nombre al espacio de almacenamiento y selecciona la letra de unidad, el sistema de archivos, el tipo de resiliencia y el tamaño del grupo, y luego selecciona Crear espacio de almacenamiento.

Cuando se crea el espacio de almacenamiento, la letra de la unidad de almacenamiento aparece en el Explorador de archivos.

### Caché de disco / Memoria virtual

Cuando compras un disco duro, una unidad óptica o una SSD, una característica que deberías considerar al elegir entre unidades es la cantidad de caché de la unidad. La caché de disco (a veces llamada búfer de datos) es SRAM en la unidad que recibe datos y los retiene allí hasta que la unidad tiene tiempo de escribirlos. La caché también se puede usar cuando se solicitan datos a la unidad. La unidad lee más datos de los solicitados y los retiene hasta que se necesitan, sin volver al disco duro. La Figura 7.44 muestra este concepto.

> Figura 7.44 Caché de disco

Otra forma de usar un disco duro es con la memoria virtual o usando el espacio del disco duro como si fuera RAM. La cantidad de RAM instalada en un sistema no es suficiente para manejar el sistema operativo y las múltiples aplicaciones que se abren y se usan. Solo el programa y los datos de la aplicación que se están usando actualmente están en la RAM. El resto de las aplicaciones abiertas y los datos se almacenan en un archivo de paginación (también llamado archivo de intercambio, swap file, pagefile.sys o archivo de página) en el disco duro. Cuando cambias a una aplicación diferente que se mantiene en el archivo de intercambio, los datos se mueven de la RAM al archivo de intercambio, y los datos que necesitas ver se mueven a la RAM para un acceso y una manipulación de datos más rápidos. La caché de disco es dinámica, lo que significa que aumenta y disminuye el tamaño de la caché según sea necesario. Si el sistema comienza a paginar (es decir, a intercambiar datos constantemente entre la RAM y el disco duro), el tamaño de la caché se reduce automáticamente. En Windows, el archivo de intercambio de memoria virtual se llama `pagefile.sys`. Así se ajusta en Windows 10/11: accede a Configuración. En el cuadro de texto de búsqueda Buscar una configuración, escribe rendimiento. Selecciona el enlace Ajustar la apariencia y el rendimiento de Windows > pestaña Avanzado > botón Cambiar (como se muestra en la Figura 7.45). Cambia los parámetros y haz clic en el botón Aceptar dos veces.

> Figura 7.45 Administrador de memoria virtual de Windows 10

### Consejo técnico: dónde mantener un archivo de intercambio

Si hay varios discos duros disponibles, un técnico podría querer mover el archivo de intercambio a una unidad diferente. Coloca el archivo de intercambio en el disco duro más rápido, a menos que a ese disco duro le falte espacio. El archivo de intercambio puede residir en varios discos duros. Es mejor mantener el archivo de intercambio en un disco duro que no contenga el sistema operativo.

El espacio de memoria se divide en bloques de memoria de 4 KB llamados páginas (pages). El sistema operativo asigna tanta RAM disponible como sea posible a una aplicación. Luego, el sistema operativo intercambia, o pagina, la aplicación hacia y desde el archivo de intercambio temporal según sea necesario. El sistema operativo determina la configuración óptima para este archivo de intercambio; sin embargo, el tamaño del archivo de intercambio se puede cambiar. El archivo de página también puede corromperse. Si se corrompe, en Windows, mantén pulsada la tecla <kbd>Shift</kbd> mientras seleccionas Reiniciar desde el icono de encendido > Solucionar problemas > Opciones avanzadas > Reparación de inicio.

### Consejo técnico: añadir más RAM física ayuda con la caché

Una de las formas más eficaces de acelerar una computadora es reducir la cantidad de datos que hay que intercambiar del disco duro a la RAM. Esto se logra aumentando la cantidad de RAM de la placa madre.

## Descripción general de la solución de problemas de dispositivos de almacenamiento

Los dispositivos de almacenamiento son críticos para los usuarios de computadoras porque contienen sus datos. Lamentablemente, los usuarios no respaldan sus datos ni su sistema con frecuencia. Blackblaze (www.blackblaze.com) realizó un estudio de más de 25,000 unidades mecánicas y descubrió que, durante un período de cuatro años, el 78% de las unidades duró más de cuatro años, pero el 22% falló durante los primeros cuatro años. Las unidades mecánicas tienen partes móviles, y las partes móviles fallan. ¡Espera que ocurra!

Las herramientas que un técnico necesita para solucionar problemas de dispositivos de almacenamiento incluyen tanto hardware como software. La siguiente lista es un buen punto de partida:

- Destornillador para aflojar o quitar tornillos.
- Caja de disco duro externo para poder comprobar una unidad desde otro sistema o poder determinar si el problema es la unidad o el puerto de la placa madre (consulta la Figura 7.4 para ver una).
- Acceso a comandos del sistema operativo y herramientas de Windows para comprobar una unidad en busca de errores físicos y de estructura de archivos, e intentar corregirlos.

Dos cosas que recordar al solucionar problemas de un dispositivo de almacenamiento son tener paciencia y ser amable con el usuario. Un técnico que trabaja con dispositivos de almacenamiento con frecuencia se enfrenta a usuarios enojados. Mantén la calma y haz lo mejor que puedas. El hecho de que un sistema no arranque desde el disco duro no significa que esté defectuoso. Hay cosas que puedes hacer, como verás pronto.

### Lidiar con un rendimiento lento

Mantener un sistema informático en un entorno operativo limpio y fresco prolonga la vida del disco duro. Los fallos del disco duro se deben a problemas con las partes móviles (cabezales y motores), fluctuaciones de energía y/o fallos. Realizar un mantenimiento preventivo de toda la computadora es bueno para todos los componentes del interior de la computadora, incluido el subsistema de disco duro.

Windows tiene tres excelentes herramientas para usar en el mantenimiento preventivo del disco duro: comprobación de errores (Comprobar ahora o el botón Comprobar), Liberador de espacio en disco (Disk Cleanup) y Desfragmentador de disco (Disk Defragmenter).

En Windows, puedes usar una herramienta de disco para localizar clústeres perdidos, que son clústeres que se han disociado de los archivos de datos pero que aún ocupan espacio en disco. La comprobación de errores/Comprobar ahora también es buena para lidiar con errores de lectura/escritura intermitentes. Localiza la unidad en el Explorador de archivos, haz clic derecho en la unidad y luego selecciona Propiedades > pestaña Herramientas > Comprobar.

El programa de Windows Liberador de espacio en disco elimina archivos temporales, elimina archivos de internet sin conexión, vacía la Papelera de reciclaje, comprime archivos no usados y elimina programas no usados, y te pregunta antes de hacer cualquiera de estas cosas. Para acceder al Liberador de espacio en disco, sigue estos pasos:

Paso 1. Accede al Explorador de archivos.

Paso 2. Haz clic derecho en la letra de unidad (comúnmente C:) y selecciona Propiedades.

Paso 3. En la pestaña General, selecciona el botón Liberador de espacio en disco.

Paso 4. En la ventana Liberador de espacio en disco, marca las casillas de las opciones deseadas y haz clic en Aceptar (como se muestra en la Figura 7.46).

> Figura 7.46 Ventana del Liberador de espacio en disco

### Consejo técnico: ejecutar el Liberador de espacio en disco desde el símbolo del sistema

Para ejecutar el Liberador de espacio en disco desde el símbolo del sistema, escribe `cleanmgr.exe` y luego pulsa <kbd>Enter</kbd>.

El rendimiento de la unidad afecta el rendimiento del sistema y de las aplicaciones. Algunos proveedores enumeran el número de operaciones de entrada/salida por segundo (IOPS) como medida del rendimiento del almacenamiento, pero esto no es una medición consistente. Si una unidad tarda en responder o tiene tiempos de lectura/escritura extendidos, puedes usar el Administrador de tareas > pestaña Rendimiento > hacer clic en la unidad y observar los datos de tiempo de respuesta promedio, velocidad de lectura y velocidad de escritura. También hay un enlace allí que puedes usar, o puedes abrir el Monitor de recursos de Windows (`resmon.exe`) > pestaña Disco para ver los detalles de los datos.

Con el tiempo, a medida que se añaden archivos a un disco duro, los archivos se fragmentan, lo que significa que los clústeres que forman un archivo no son adyacentes entre sí. La fragmentación ralentiza un disco duro de dos maneras: la FAT tiene que realizar un seguimiento de los clústeres dispersos, y el conjunto de cabezales de lectura/escritura del disco duro debe moverse a diferentes ubicaciones de la superficie de la unidad para acceder a un solo archivo. La Figura 7.47 ilustra la fragmentación de tres archivos (F1, F2 y F3) y los resultados después de que se ha ejecutado la desfragmentación en el disco duro. La desfragmentación es el proceso de colocar los archivos en sectores contiguos. Observa los resultados del proceso de desfragmentación en la Figura 7.47:

> Figura 7.47 Disco duro fragmentado / disco duro desfragmentado

### Consejo técnico: el orden de las herramientas importa

Usa las herramientas de comprobación de errores (Comprobar ahora o Comprobar) y Liberador de espacio en disco antes de ejecutar la herramienta Desfragmentador de disco.

- Desfragmentar un disco duro hace que el acceso al disco duro sea más rápido. Este proceso también prolonga la vida del disco duro al reducir los movimientos mecánicos de la unidad. Windows 7 programa automáticamente la desfragmentación de un disco duro todos los miércoles a la 1 a. m. Windows 8 y superiores realizan la optimización del disco duro según sea necesario. Puedes ejecutar manualmente la optimización usando la herramienta Desfragmentador de disco.
- En Windows, abre el Explorador de archivos, localiza una letra de disco duro, haz clic derecho en ella y selecciona Propiedades > pestaña Herramientas > Optimizar.
- Desde el símbolo del sistema o el cuadro de búsqueda, usa el comando `defrag`.
- Desde el símbolo del sistema o el cuadro de búsqueda, usa el comando `dfrgui.exe`.

### Consejo técnico: la desfragmentación mata a las SSD

No desfragmentes una SSD como lo harías con un disco duro magnético. La desfragmentación provoca más lecturas y escrituras, lo que reduce la vida útil de la SSD.

### Pérdida y corrupción de datos

Un disco duro normalmente tiene una garantía de tres años, pero las personas usan sus computadoras más tiempo que eso. Los discos duros fallan y los datos se pierden o se corrompen. La mejor prevención es respaldar la unidad. Puedes comprar una unidad que respaldará toda tu unidad con un solo clic. También puedes usar almacenamiento en la nube gratuito, como Google Drive o Microsoft OneDrive, para el almacenamiento de datos desde una variedad de dispositivos de almacenamiento.

En el mundo corporativo, las empresas pueden comprar software de recuperación de archivos o contratar a otras empresas que lo proporcionen como servicio. Los técnicos que no tienen este software deberían al menos tener el nombre de una empresa que recomienden o usen.

Los discos duros tienen tecnología integrada para marcar sectores defectuosos y mover los datos a una ubicación diferente de la unidad. Esos datos pueden corromperse aunque se muevan. Aquí hay algunas recomendaciones para reparar datos corruptos.

- Restaura los datos corruptos desde una copia de seguridad.
- Si se trata de uno o varios archivos del sistema, usa la herramienta System File Checker con el comando `sfc /scannow`.
- Si el comando sfc no funciona, puedes reinstalar el sistema operativo usando la opción Actualizar tu PC (Refresh your PC), que conserva las aplicaciones que venían con la PC y las aplicaciones instaladas desde Microsoft Store. También puedes usar la opción Restablecer este PC (Reset this PC), que te permite elegir si conservar tus archivos personales. Ten en cuenta que sí tienes que reinstalar tus aplicaciones.
- Usa el comando `chkdsk`. Usa la opción /f para corregir cualquier error encontrado en el disco. Usa la opción /R para localizar sectores defectuosos y recuperar cualquier información legible.

### Solución de problemas de instalación de nuevos dispositivos de almacenamiento

La mayoría de los problemas con la instalación de una unidad nueva provienen de una configuración incorrecta de los puentes en las unidades PATA o de problemas con el cableado. La BIOS/UEFI y el sistema operativo pueden mostrar una multitud de síntomas, incluidos códigos de error de POST, pitidos y mensajes, como los siguientes:

- Hard drive not found (Disco duro no encontrado)
- No boot device available (No hay dispositivo de arranque disponible)
- Hard drive not present (Disco duro no presente)
- Inaccessible boot device (Dispositivo de arranque inaccesible)
- Invalid boot disk (Disco de arranque no válido)

Los siguientes consejos ayudan a comprobar posibles problemas cuando ocurren errores de «unidad no reconocida» en el sistema o un LED de la placa madre indica un fallo de unidad o de arranque:

- Comprueba la configuración física (como el cable de alimentación, la configuración de los puentes, el cable de datos seguro, la orientación del pin 1 del cable de datos y la ubicación del dispositivo en el cable de datos).
- Comprueba la configuración del tipo de unidad en la configuración de la BIOS/UEFI y asegúrate de que los puertos (especialmente los puertos SATA) estén habilitados.
- Si todo funciona bien, pero el LED de actividad de la unidad no parpadea al almacenar/recuperar datos, comprueba la conexión del cable del panel frontal a la placa madre.
- Si después de configurar la unidad, instalarla y encenderla, la BIOS/UEFI muestra el tipo de unidad como «None» o «Not installed», o muestra todos los 0 en los parámetros de la unidad aunque la configuraste para detectar automáticamente la unidad, entonces la BIOS/UEFI no puede detectarla. Comprueba el modo SATA de la BIOS/UEFI y la versión de la BIOS/UEFI. Comprueba todas las configuraciones de los puentes, comprueba las conexiones de los cables y comprueba la conexión de alimentación. En la configuración, reduce cualquier función avanzada a sus valores más bajos o desactívalas. Aumenta la cantidad de tiempo que tarda la computadora en inicializar el disco duro entrando en la configuración y modificando funciones como el retardo de arranque del disco duro o ajustando la velocidad de arranque al valor más bajo. Esto le da al disco duro más tiempo para girar y alcanzar las RPM adecuadas antes de que se lean los datos. Asegúrate de que el puerto de la placa madre esté habilitado.
- Si la BIOS/UEFI reconoce el dispositivo pero tienes una unidad faltante en el SO, es posible que la unidad no se haya inicializado o particionado. Usa la herramienta Administración de discos de Windows para solucionarlo.
- Determina si la unidad ha sido particionada y si una partición ha sido marcada como la partición activa. Determina también si se ha aplicado el formato de alto nivel a la unidad.
- Si el disco duro no se formatea a su capacidad total, es posible que tu BIOS/UEFI no admita la unidad más grande y/o que la BIOS/UEFI deba actualizarse, que hayas seleccionado un sistema de archivos que no admite particiones más grandes, o que necesites un controlador actualizado.
- Si durante el encendido el disco duro no gira o si el disco duro se detiene después de unos segundos, comprueba el conector de alimentación, el cable de datos, la unidad reconocida en la BIOS/UEFI, la configuración de los puentes, los puentes o la configuración de administración de energía en la configuración y cualquier software que viniera con la unidad que habilite la administración de energía. Desactiva la administración de energía en la BIOS/UEFI y/o en el sistema operativo. Intenta instalar la unidad en otro sistema.
- Si el sistema se bloquea o aparece una pantalla azul de la muerte (BSOD), anota el mensaje o el código, si lo hay, e intenta un reinicio en caliente (<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Supr</kbd>). Si la unidad es reconocida después del reinicio en caliente, es posible que el programa de configuración se esté ejecutando demasiado rápido para que la unidad se inicialice. Consulta la documentación del disco duro para ver si el disco duro tiene una configuración que ayude con este problema.
- Verifica que el tornillo de montaje para sujetar la unidad en la carcasa no esté demasiado apretado. Afloja el tornillo y enciende la computadora. La Figura 7.48 muestra los tornillos de montaje de un disco duro instalado en una carcasa de torre.

> Figura 7.48 Tornillos de montaje del disco duro

### Solución de problemas de dispositivos de almacenamiento previamente instalados

Los dispositivos de arranque previamente instalados pueden tener todos los mismos síntomas que un dispositivo de almacenamiento recién instalado, más los siguientes:

- Sonidos de clic (clicking sounds)
- Errores de lectura/escritura
- Respuesta lenta
- Pantalla azul de la muerte (BSOD) o molinillo (pinwheel) (macOS y Windows)

Como muchas unidades son dispositivos mecánicos, hacen ruidos. A veces estos ruidos ocurren porque el disco duro se usa demasiado como memoria virtual debido a la falta de RAM física. Algunos ruidos son normales y otros indican problemas, como se muestra en la Figura 7.49.

> Figura 7.49 Ruidos del disco duro

Cuando un disco duro comienza a hacer ese fuerte ruido de clic, golpeteo o chirrido, respalda la unidad inmediatamente y compra una unidad de reemplazo. ¡La unidad está fallando!

Las siguientes son pautas genéricas para discos duros que han funcionado pero que ahora tienen problemas o para cuando una computadora no arranca:

- Ejecuta un programa antivirus después de arrancar desde medios de arranque libres de virus. Muchos virus están diseñados específicamente para atacar discos duros. Si tienes que borrar un disco duro para asegurarte de que el virus se elimina antes de reinstalar el sistema operativo, las aplicaciones y los datos, asegúrate de hacer un formato completo y no uno rápido como parte del proceso de instalación del sistema operativo.
- ¿Ha habido una limpieza reciente de la computadora, o alguien ha quitado recientemente la tapa de la computadora? Si es así, comprueba todos los cables y verifica que se conecten correctamente. Comprueba la conexión de alimentación del disco duro.

### Consejo técnico: ¿se atasca tu disco duro?

Coloca una mano sobre la parte superior de la unidad mientras enciendes la computadora. ¿Gira la unidad en absoluto? Si no, el problema es probablemente una unidad «pegada» o una unidad defectuosa. Un disco duro debe girar a cierta RPM antes de que los cabezales se muevan sobre la superficie del disco duro. Para comprobar si la unidad se está atascando, quita la unidad e intenta girar el motor del husillo a mano. Si no se mueve, quita la unidad, sostenla en tu mano y da un tirón rápido con la muñeca. Otro truco que puede funcionar es quitar el disco duro de la carcasa, colocar la unidad en una bolsa de plástico y ponerla en el congelador durante un par de horas. Luego quita la unidad, deja que se caliente a temperatura ambiente, vuelve a instalarla en el sistema e inténtalo.

- Si la luz del disco duro parpadea rápidamente al arrancar, el controlador está intentando leer la tabla de particiones en el registro de arranque maestro. Si no se encuentra esta información, son posibles varios síntomas, como los mensajes de error «Invalid boot disk», «Inaccessible boot device», «Invalid partition table», «Error loading operating system», «Missing operating system» o «No operating system found». Usa el comando `diskpart` desde el Entorno de recuperación de Windows (WinRE) para ver si la tabla de particiones del disco duro está bien. Aquí hay algunos comandos para probar dentro de esta utilidad: `list disk`, `list volume`, `list partition`, `detail disk`, `detail volume` y `detail partition`. Intenta ejecutar `bootrec /fixmbr` o usa una utilidad de disco duro para reparar la tabla de particiones.
- Un problema común es que no se puede encontrar el sistema operativo, lo que se indica con el mensaje bootable device not found o no OS found (u otros mensajes, como «Disk Boot Failure», «Non-System Disk» y «Disk Error» que pueden indicar un problema en el registro de arranque). La solución es arrancar desde un disco de arranque o una unidad flash USB para ver si la unidad C: está disponible. Al hacerlo, cambia la configuración del orden de arranque de la BIOS/UEFI para arrancar desde tu medio extraíble. Es posible que haya que recargar el sistema operativo. Además, verifica que la partición primaria esté marcada como activa y que no haya medios no arrancables, como un disco o una unidad flash USB, insertados o conectados al sistema. Comprueba la configuración de la primera opción de arranque en la BIOS/UEFI y asegúrate de que esté configurada en la unidad adecuada.
- Si recibes un mensaje como «Hard drive not found», «No boot device available», «Fixed disk error» o «Disk boot failure», la BIOS/UEFI no puede encontrar el disco duro. Comprueba el cableado. Coloca la unidad en una caja externa y conéctala a una computadora que funcione.
- Si aparece un error de self-monitoring, analysis, and reporting technology (S.M.A.R.T.), respalda los datos e investiga el error para tomar medidas inmediatas. S.M.A.R.T. se usa para monitorizar tanto los discos duros mecánicos como las SSD. Un error de S.M.A.R.T. puede aparecer inmediatamente antes de un fallo. La Tabla 7.10 enumera algunos de los errores de S.M.A.R.T. Ten en cuenta que los fabricantes de unidades también pueden tener sus propios errores.

**Tabla 7.10 Errores de S.M.A.R.T.**

| Error | Descripción |
| --- | --- |
| Recuento de sectores reasignados (Reallocated sectors count) | El número de sectores que se marcaron como defectuosos, lo que provocó que los datos dentro de esos sectores se movieran. |
| Reintento de giro (Spin retry) | El número de veces que la unidad no alcanzó la velocidad suficiente para leer y escribir desde la unidad. |
| Recuento de errores de reducción de velocidad de SATA o recuento de bloques defectuosos en tiempo de ejecución | El número de bloques de datos que contenían errores incorregibles. |
| Errores incorregibles reportados (Reported uncorrectable errors) | El número de errores incorregibles detectados. |
| Evento de reasignación (Reallocation event) | Cuántas veces hubo que reasignar datos. |
| Tasa de errores de lectura suave o contador TA | El número de errores de desvío de pista (off-track) detectados. |

- Cuando Windows tiene problemas de inicio, se usan el Entorno de recuperación de Windows (WinRE) y el menú de Opciones avanzadas (pulsa <kbd>F8</kbd> al iniciar). Con los dispositivos Windows, si el sistema arranca demasiado rápido como para acceder a este menú, mantén pulsada la tecla <kbd>Shift</kbd> mientras reinicias el sistema. Luego selecciona Solucionar problemas > Opciones avanzadas > Reparación de inicio o Símbolo del sistema. Los problemas de inicio a menudo se deben a virus. Otras utilidades que ayudan con el MBR, el sector de arranque y los archivos del sistema son System File Checker (SFC) y el menú de Opciones de arranque avanzadas. Usa `bootrec /fixmbr` o `bootrec /fixboot` desde WinRE.

### Consejo técnico: usar System File Checker

Puedes ejecutar el programa System File Checker desde el símbolo del sistema escribiendo `sfc /scannow`. El System File Checker también debe ejecutarse después de eliminar algunos virus.

- Cuando Windows tiene problemas de inicio debido a hardware o software incompatible o a un proceso de instalación corrupto, el menú de Opciones de arranque avanzadas puede ayudar.
- Si aparece un error de espacio en disco insuficiente o si el usuario experimenta un rendimiento lento (es decir, si la computadora tarda mucho en responder), elimina los archivos innecesarios, incluidos los archivos .tmp, del disco duro, vacía la Papelera de reciclaje y guarda los archivos en un disco óptico, una unidad flash o un disco duro externo, y elimina del disco duro los archivos movidos. Usa las herramientas Liberador de espacio en disco y Desfragmentador. Otra opción es añadir otro disco duro y mover algunos (o todos) los archivos de datos a él.
- Para las unidades eSATA, comprueba el cableado de alimentación y el cableado de datos. Asegúrate de que el cable de datos sea del tipo correcto para el puerto y el dispositivo que se está usando. Particiona y formatea la unidad antes de que se escriban datos en ella. Asegúrate de que el puerto esté habilitado a través de la BIOS. Es posible que la BIOS/UEFI requiera una actualización, o que se requiera un controlador de dispositivo (especialmente si la unidad aparece en Otros dispositivos en el Administrador de dispositivos). Ten en cuenta que algunos sistemas operativos reportan las unidades SATA como unidades SCSI.
- Si la computadora informa que el disco duro puede tener un área defectuosa o si comienzas a recibir avisos de fallo de lectura/escritura, haz clic derecho en el volumen del disco duro > Propiedades > pestaña Herramientas > Comprobar ahora (Windows 7)/Comprobar (8/10). Es posible que haya que reemplazar la unidad pronto.
- Si las unidades fallan con frecuencia en una computadora en particular, comprueba si hay problemas de calor, fluctuaciones de energía, vibraciones, tornillos o hardware de montaje inadecuados que puedan causar vibraciones, y problemas ambientales como polvo, calor, campos magnéticos, humo y motores cercanos. Considera usar una SSD si la computadora está en un entorno hostil.
- Si una unidad USB es el dispositivo de arranque y el sistema no arranca, desenchufa la unidad, vuelve a conectarla y reinicia el sistema.
- Si aparece un molinillo, pelota, reloj de arena u otro icono específico de la aplicación; si aparece un mensaje de que una aplicación no responde (a veces preguntándote si quieres esperar o finalizar la aplicación); o si una unidad tarda mucho en responder dentro de una aplicación, usa la herramienta Administración de discos para ver el estado de la unidad. (Ten en cuenta que el molinillo de color de Mac se trata en el Capítulo 17). La Tabla 7.11 muestra algunos de los mensajes de estado de unidad, normales y con problemas, que se ven en la herramienta Administración de discos de Windows. Estos mensajes de estado pueden ayudar con la administración, la solución de problemas y la recuperación de la unidad.

**Tabla 7.11 Estados de estado de Administración de discos**

| Estado | Descripción |
| --- | --- |
| Activo (Active) | La partición de arranque, generalmente en el primer disco duro, está lista para usarse. |
| Dinámico (Dynamic) | Como alternativa al disco básico, el disco dinámico tiene volúmenes en lugar de particiones. Los tipos de volúmenes incluyen volúmenes simples, volúmenes que abarcan más de una unidad y volúmenes RAID. |
| Con errores (Failed) | El disco básico o el volumen dinámico no pueden iniciarse; el disco o el volumen podrían estar dañados; el sistema de archivos podría estar corrupto; o puede haber un problema con el disco físico subyacente (encendido, cableado correctamente) o con una unidad RAID asociada. Haz clic derecho en el disco y selecciona Reactivar disco (Reactivate Disk). Haz clic derecho en el volumen dinámico y selecciona Reactivar volumen (Reactivate Volume). |
| Externo (Foreign) | Se acaba de instalar un disco dinámico de otra computadora. Haz clic derecho en el disco y selecciona Importar discos externos (Import Foreign Disks). |
| Correcto (Healthy) | La unidad está lista para usarse. |
| No inicializado (Not Initialized) | Un disco básico no está listo para usarse. Haz clic derecho en el disco y selecciona Inicializar disco (Initialize Disk). La opción Inicializar disco habilita un disco para que se puedan almacenar datos. |

### Problemas de RAID

Cuando se configuran dos o más unidades en un RAID, se ven como un solo volumen y se administran como un solo volumen. Debido a los diferentes tipos de RAID y al número de discos duros involucrados en el RAID, pueden ocurrir muchos problemas. Los síntomas de los problemas de RAID son similares a los que ocurren con un fallo de disco duro (fallo de lectura/escritura, partición RAID perdida, rendimiento lento del sistema, fuerte ruido de clic, fallo al arrancar, unidad no reconocida, sistema operativo no encontrado o una BSOD).

Los siguientes problemas pueden ayudarte con las configuraciones de RAID:

- Si has hecho RAID a través de la BIOS/UEFI, no puedes administrar RAID a través de Windows (aparece atenuado y se muestra como sin tolerancia a fallos). Si quieres administrar RAID a través de Windows, tienes que romper el RAID en la BIOS/UEFI (quitar el RAID) y luego volver a crear el RAID en Windows. Haz una copia de seguridad de tus datos antes de hacer esto.
- A veces, como parte de la configuración de RAID, necesitas medios de controlador para la instalación de Windows o el proceso de solución de problemas de fallos de RAID. Sigue las instrucciones de fabricación de la placa madre o del adaptador RAID sobre cómo crear estos medios (generalmente mediante una unidad USB o un disco óptico, aunque las instrucciones en pantalla puedan decir disquete).
- Si Windows no te permite o no te da la opción de crear una matriz RAID, comprueba la configuración de la BIOS/UEFI y asegúrate de que AHCI se haya habilitado para las unidades.
- Si la duplicación de discos no es una opción en la Administración de discos de Windows, comprueba tu versión de Windows. Debes tener Windows Professional o una edición superior para crear una matriz RAID.
- Si Windows ya no arranca, aparece una BSOD y la unidad de arranque de Windows forma parte de una matriz RAID, reinstala Windows si quieres conservar la matriz RAID. Es posible que tengas que obtener controladores antes de hacer esto. Si no te importa el RAID y solo quieres que Windows arranque de nuevo, quita el RAID por hardware. También puedes usar el código de BSOD mostrado para investigar el error.
- Si una partición RAID desaparece repentinamente, comprueba si hay un virus.
- Si recibes un mensaje como RAID not found, comprueba la configuración de hardware o software (según el tipo de RAID que se haya configurado). Una subida de tensión puede corromper una configuración de RAID por hardware realizada a través de la configuración de la BIOS/UEFI. Una actualización del sistema, una actualización de la aplicación o una nueva aplicación pueden afectar al RAID por software.
- Si tienes un fallo de RAID, usa la herramienta Administración de discos de Windows para comprobar el estado de las unidades. Luego comprueba la configuración de RAID si las unidades están bien.

### Problemas de SSD

La BIOS debería reconocer una SSD instalada internamente. Si no lo hace, entra en la configuración de la BIOS/UEFI del sistema y asegúrate de que el conector al que se conecta la SSD esté habilitado. Ten especial cuidado con los puertos SATA y la numeración de puertos. Configura el sistema para que detecte automáticamente la nueva unidad, guarda la configuración y reinicia el sistema. Aquí hay algunas cosas que probar, pero recuerda que también se aplican otros consejos sobre discos duros, como los relacionados con que la computadora no arranque o no se encuentre el sistema operativo:

- Reinicia el PC.
- Prueba otro puerto o cable SATA.
- Desinstala/reinstala el controlador.
- Usa software de clonación del fabricante de la SSD o comprado a otro proveedor.
- Desactiva la opción de BIOS Wake on LAN.

## Habilidades interpersonales: habilidades telefónicas

Los técnicos con frecuencia deben usar el teléfono en el curso normal de su trabajo para hablar con clientes, proveedores y personal de soporte técnico. El trabajo de un técnico puede implicar la comunicación por teléfono a tiempo completo.

Las habilidades de comunicación telefónica son diferentes de las habilidades necesarias para la comunicación en persona porque por teléfono solo tienes tus palabras y la entonación de tu voz para transmitir conceptos, profesionalismo y asistencia técnica. Cuando tratas con alguien en persona, puedes usar algunas de las siguientes técnicas que no son tan eficaces en una conversación telefónica:

- Hacer gestos para enfatizar puntos.
- Dibujar un gráfico para ilustrar un concepto.
- Realizar los pasos necesarios para la solución de problemas más rápido, porque puedes hacerlos en lugar de guiar a alguien a través de ellos.
- Mostrar empatía más fácilmente con tu lenguaje corporal, tus acciones y tu voz.

Cuando trates con alguien por teléfono, los siguientes consejos pueden ayudar. Algunos de los consejos también se aplican al soporte técnico cotidiano:

- Identifícate de forma clara y agradable.
- Sonríe aunque no puedan verte (ver la Figura 7.50). Marcará la diferencia en tu tono.

> Figura 7.50 Habilidades de comunicación telefónica

- Evita usar un tono condescendiente.
- Sé paciente y habla despacio cuando des instrucciones.
- Usa habilidades de escucha activa (tratadas en el Capítulo 2, «Conectividad»); evita hacer otras tareas cuando estés en una llamada con alguien.
- Evita usar siglas y jerga técnica.
- Evita ser acusador o amenazante.
- Si el cliente está furioso, intenta calmarlo y ayudarlo; sin embargo, si el cliente sigue siendo beligerante, pasa la llamada a tu supervisor.
- Escala el problema si está más allá de tu nivel de habilidad; no hagas perder el tiempo al cliente.
- No dejes a las personas en espera durante períodos prolongados sin volver a contactarlas y actualizarlas.
- Habla con claridad y con la suficiente intensidad para que te oigan fácilmente.
- Evita tener el micrófono del auricular alejado de modo que sea difícil oírte; si te piden que repitas algo, habla más alto o ajusta el micrófono o el auricular.
- Evita comer, beber o masticar chicle cuando estés al teléfono.

Las buenas habilidades interpersonales son aún más importantes por teléfono que en las interacciones cara a cara. Antes de ponerte al teléfono, respira profundamente y revisa tu actitud. Cada cliente merece tu mejor esfuerzo, sin importar qué tipo de día hayas tenido o con qué tipo de cliente hayas hablado antes.

## Resumen del capítulo

- Los factores de forma de los discos duros incluyen unidades de 5.25, 3.5, 2.5 y 1.8 pulgadas. Los discos duros vienen en diferentes velocidades: 5,400, 7,200, 10,000 y 15,000 RPM. Las tasas de RPM más rápidas significan discos duros más caros, pero también transferencias de datos más rápidas.
- Las unidades comunes hoy en día son PATA, SATA y SSD para computadoras de escritorio y móviles.
- Una unidad PATA es solo interna y se conecta a un cable plano de 40 pines que puede tener dos dispositivos por conector/cable de la placa madre.
- Las unidades SATA pueden ser internas o externas y se conectan usando un conector interno de 7 pines de 3.3 pies (1 metro) como máximo, un conector eSATA externo (3.3 pies [1 metro] como máximo para dispositivos de 1.5 Gb/s y 6.56 pies [2 metros] como máximo para dispositivos de 3 o 6 Gb/s), o un puerto combo eSATAp eSATA/USB. Las unidades SATA 1 (I) funcionan a un máximo de 1.5 Gb/s, las unidades SATA 2 (II) a 3 Gb/s y las unidades SATA 3 (III) a 6 Gb/s. Las unidades SATA internas usan un conector de alimentación SATA exclusivo. Se puede comprar un convertidor de Molex a SATA, pero no se suministran 3.3 V a la unidad; la mayoría de las unidades no usan la línea de 3.3 V. Las unidades externas usan una fuente de alimentación externa a menos que se enchufen a un puerto combo eSATAp, que puede proporcionar alimentación.
- Una unidad SATA no requiere puente, y solo un dispositivo puede conectarse a un puerto SATA de placa madre/adaptador.
- Las SSD se han vuelto más comunes en computadoras de escritorio, portátiles y tabletas. A menudo se usan en entornos hostiles, entornos sucios, entornos con mucho movimiento y entornos de temperaturas extremas. Son extremadamente rápidas pero caras. Se conectan mediante conexiones SATA, mSATA, eSATA, M.2, PCIe o USB.
- Las SSD borran datos en bloques en lugar de marcar clústeres disponibles en la FAT como las unidades tradicionales. Las SSD no deben desfragmentarse. Las SSD usan varias tecnologías para garantizar su funcionalidad, como usar toda la memoria de manera uniforme (nivelación de desgaste, wear leveling) y usar bloques de memoria de reserva.
- Una SSHD es una combinación de un disco duro mecánico y memoria flash que contiene los datos usados con más frecuencia.
- Los discos duros deben particionarse y tener aplicado el formato de alto nivel antes de que puedan usarse para almacenar datos.
- El particionado separa una unidad en secciones más pequeñas (volúmenes) que pueden recibir letras de unidad. Cuanto más pequeño es el volumen, más pequeño es el tamaño del clúster. Un clúster es el espacio más pequeño en el que puede residir un solo archivo. Un clúster consta de cuatro o más sectores, y cada sector contiene 512 bytes.
- El particionado se puede hacer a través del proceso de instalación de Windows o usando la herramienta Administración de discos.
- Un volumen simple es el tipo más común de volumen de partición creado.
- Para crear un volumen distribuido (también conocido como JBOD), el espacio de dos o más discos duros se ve como una sola letra de unidad. Se llena una unidad antes de usar cualquier otro disco duro.
- Un volumen seccionado escribe datos en dos o más unidades, pero no proporciona redundancia.
- El volumen del sistema (generalmente C:) contiene los archivos necesarios para arrancar el sistema operativo.
- El volumen de arranque (generalmente C:) contiene la mayoría de los archivos del sistema operativo.
- Los fabricantes de computadoras pueden usar un HPA o una partición protegida para la recuperación del sistema.
- Se pueden configurar varias unidades en una implementación de RAID por hardware o software. El RAID por hardware se hace usando la BIOS/UEFI o un adaptador RAID. El RAID por software se hace usando la herramienta Administración de discos de Windows.
- RAID 0, o seccionado de discos, no proporciona tolerancia a fallos, pero sí proporciona un uso rápido y eficiente de dos o más unidades.
- RAID 1 es la duplicación de discos, y este método sí proporciona tolerancia a fallos al garantizar una copia exacta de una unidad en caso de que una falle.
- RAID 5 es el seccionado de discos con paridad, donde los datos de paridad se mantienen en una de las tres o más unidades. Estos datos de paridad se pueden usar para reconstruir una unidad si una de las tres o más unidades falla.
- RAID 10 es un conjunto duplicado y un conjunto seccionado combinados con un mínimo de cuatro discos duros. Este modo puede leer del disco rápidamente pero con una ligera degradación al escribir.
- Los Espacios de almacenamiento de Windows pueden usar una variedad de tipos de unidades para crear un único espacio de almacenamiento que puede tener cualidades similares a RAID.
- Los sistemas de archivos en uso son FAT16 (FAT), FAT32, exFAT, NTFS, APFS, ext3 y ext4. FAT32 y exFAT se usan para unidades externas, como unidades flash USB. NTFS, que se usa para unidades internas, proporciona características como mejor administración de clústeres, seguridad, compresión y cifrado. ext3 y ext4 se usan en sistemas basados en Linux.
- Dos formas de cambiar de un sistema de archivos a otro son usar el comando convert y formatear la unidad. El comando convert conserva los datos existentes. El formato de alto nivel no conserva ningún dato guardado.
- Si una unidad no se reconoce como una instalación nueva, comprueba el cableado y la configuración de la BIOS/UEFI, especialmente en el caso de un puerto SATA deshabilitado.
- Los ruidos normales de una unidad mecánica incluyen un clic al entrar en modo de suspensión o al apagarse debido al autoestacionamiento de los cabezales.
- Los ruidos anormales de una unidad incluyen un par de clics con un pitido y/o error de POST, ruidos de clic repetidos, ruido de chirrido, vibración de alta frecuencia debido a hardware de montaje inadecuado o deficiente, y un sonido agudo de zumbido.
- Si una unidad falla después de funcionar durante un tiempo, comprueba si hay un virus. Mira si la BIOS tiene un verificador de virus. Prueba un reinicio en caliente para ver si la unidad aún no ha alcanzado la velocidad. Comprueba el cableado, especialmente en SATA. Revisa cualquier cambio reciente. Usa el menú de Opciones de arranque avanzadas de Windows, el Entorno de recuperación de Windows (WinRE), System File Checker (SFC) y los comandos `bootrec /fixmbr` y `bootrec /fixboot`. Arranca desde una fuente alternativa y comprueba la Administración de discos en busca de mensajes de estado relacionados con el disco duro.
- El espacio del disco duro usado como RAM se conoce como memoria virtual. Asegúrate de que haya suficiente espacio de almacenamiento libre disponible.
- Cuando hables por teléfono con cualquier persona, sé claro en tus afirmaciones, no uses jerga técnica, mantén un tono profesional y no hagas otras tareas, incluido comer o beber.

## Consejos para el examen de certificación A+

- Sé capaz de seleccionar, instalar y configurar unidades SATA y SSD (mSATA, PCIe, M.2 y NVMe).
- Asegúrate de conocer y poder reconocer el cableado SATA, eSATA, IDE (PATA) y SCSI (SAS).
- Sé capaz de recomendar un disco duro según la velocidad (5,400, 7,200, 10,000 y 15,000 RPM) o el factor de forma (2.5 pulgadas vs. 3.5 pulgadas).
- Sé capaz de recomendar una SSD según la interfaz usada (NVMe, SATA o PCIe), así como el factor de forma (M.2 o mSATA).
- Conoce los propósitos de las herramientas de comprobación de errores (Comprobar ahora/Comprobar), Liberador de espacio en disco y Desfragmentador de disco.
- Usa una computadora para revisar las herramientas de disco y cómo acceder a ellas.
- Revisa todos los consejos de solución de problemas justo antes de hacer el examen.
- Familiarízate con los siguientes conceptos de Administración de discos: comprender el estado de la unidad y qué hacer si el estado no es correcto (healthy), montar, extender particiones, dividir particiones, asignar letras de unidad, añadir unidades y añadir matrices.
- Conoce cómo suena un disco duro normal y qué sonidos hace un disco duro con problemas. Asegúrate de respaldar los datos antes de que falle una unidad.
- Conoce la diferencia entre los niveles de RAID 0, 1, 5 y 10.
- Conoce los diversos sistemas de archivos, incluidos exFAT, FAT32, NTFS, APFS, ext3 y ext4.
- Conoce la diferencia entre un formato rápido y un formato completo.
- Conoce las diferencias entre discos básicos y dinámicos y comprende las particiones y volúmenes primarios, extendidos y lógicos.
- Sé capaz de solucionar los síntomas comunes, como fallos de lectura/escritura, rendimiento lento, ruidos de chirrido, sonidos de clic, fallo al arrancar, unidad no encontrada o no reconocida, unidades faltantes en el SO, RAID not found y RAID que no funciona.
- Conoce la diferencia entre el comportamiento normal del LED de actividad de la unidad y el comportamiento inusual. Ten en cuenta que algunas placas madre tienen LED que pueden ayudar al solucionar problemas de unidades.
- Familiarízate con las pantallas de fallo propietarias BSOD y molinillo.
- Conoce cómo y cuándo usar las herramientas de línea de comandos de Microsoft, como `format`, `diskmgmt.msc`, `resmon.exe`, `cleanmgr.exe`, `dfrgui.exe`, `diskpart`, SFC y `chkdsk`.
- Instala un par de unidades de práctica para el examen. Configura mal la BIOS/UEFI y deja un cable desenchufado o la alimentación de la unidad quitada para que veas los errores y síntomas del POST.
- Conoce cómo y cuándo configurar RAID y las diferencias entre los distintos niveles de RAID.
- Sé capaz de inicializar una unidad, convertir un sistema de archivos, convertir una unidad a disco dinámico, crear un volumen simple y seleccionar un sistema de archivos en particular.
- Conoce cómo hablar por teléfono de manera profesional.

## Términos clave

- 10,000 RPM
- 15,000 RPM
- 2.5-inch drive (unidad de 2.5 pulgadas)
- 3.5-inch drive (unidad de 3.5 pulgadas)
- 5,400 RPM
- 7,200 RPM
- APFS
- basic disk (disco básico)
- basic storage (almacenamiento básico)
- boot partition (partición de arranque)
- boot sector (sector de arranque)
- boot volume (volumen de arranque)
- bootable device not found (dispositivo de arranque no encontrado)
- bootrec
- BSOD
- chkdsk
- clicking sound (sonido de clic)
- cluster (clúster)
- convert (convertir)
- DBR
- defrag (desfragmentar)
- defragmentation (desfragmentación)
- dfrgui.exe
- disk cache (caché de disco)
- Disk Cleanup (Liberador de espacio en disco)
- Disk Management (Administración de discos)
- disk mirroring (duplicación de discos)
- disk striping (seccionado de discos)
- diskpart
- drive activity LED (LED de actividad de la unidad)
- drive not recognized (unidad no reconocida)
- drive status (estado de la unidad)
- dynamic disk (disco dinámico)
- dynamic storage (almacenamiento dinámico)
- eSATA
- exFAT
- ext3
- ext4
- extended partition (partición extendida)
- extended read/write time (tiempo de lectura/escritura extendido)
- fail to boot (fallo al arrancar)
- FAT (file system type) (FAT [tipo de sistema de archivos])
- FAT (file allocation table) (FAT [tabla de asignación de archivos])
- FAT32
- file recovery software (software de recuperación de archivos)
- file system (sistema de archivos)
- format (formato)
- full format (formato completo)
- GPT
- grinding noise (ruido de chirrido)
- head crash (choque de cabezal)
- high-level formatting (formato de alto nivel)
- HPA
- IDE
- IDE cable (cable IDE)
- Initialize Disk (Inicializar disco)
- IOPS
- JBOD
- logical drive (unidad lógica)
- lost cluster (clúster perdido)
- M.2
- MBR
- missing drive in the OS (unidad faltante en el SO)
- motherboard LED (LED de la placa madre)
- mount (montar)
- mSATA
- MTBF
- NAS drive (unidad NAS)
- no OS found (no se encontró el SO)
- NTFS
- NVMe
- partitioning (particionado)
- phone communication skills (habilidades de comunicación telefónica)
- primary partition (partición primaria)
- quick format (formato rápido)
- RAID
- RAID 0
- RAID 1
- RAID 5
- RAID 10
- RAID failure (fallo de RAID)
- RAID not found (RAID no encontrado)
- RAW volume (volumen RAW)
- read/write failure (fallo de lectura/escritura)
- SAS
- SATA
- SATA cable (cable SATA)
- SCSI cable (cable SCSI)
- sfc
- simple volume (volumen simple)
- sluggish performance (rendimiento lento)
- S.M.A.R.T.
- spanned volume (volumen distribuido)
- spinning pinwheel (molinillo giratorio)
- SSD
- SSHD
- striped volume (volumen seccionado)
- System File Checker (Comprobador de archivos de sistema)
- system partition (partición del sistema)
- system volume (volumen del sistema)
- volume (volumen)
- Windows Storage Spaces (Espacios de almacenamiento de Windows)

## Preguntas de repaso

Considera las siguientes especificaciones de disco duro interno al responder las preguntas 1 a 7:

- Velocidad de transferencia SATA de 6 Gb/s
- Capacidad de 1 TB
- Minimiza el ruido a niveles cercanos al umbral de audición humana
- 3.5 pulgadas, 7,200 RPM
- Tamaño de búfer de 32 MB

1. ¿Qué versión de SATA se está usando?
   [ 1 | 2 | 3 | no se puede determinar con la información proporcionada ]

2. ¿Qué sistema de archivos de Windows debería colocarse en esta unidad si se va a usar cifrado?
   [ exFAT | FAT | FAT32 | NTFS ]

3. ¿Qué pasos de preparación de la unidad deben realizarse si esta unidad se añade como una unidad nueva? (Selecciona todos los que correspondan.)
   [ desfragmentación | formato de bajo nivel | formato de alto nivel | comprobación de errores | RAID | comprobación de virus | particionado | seccionado | duplexación ]

4. Se supone que esta unidad es silenciosa. Enumera dos ruidos que la unidad podría hacer y que te indicarían problemas.

5. ¿Esta unidad es interna o externa? Explica tu razonamiento.
   [ Interna | Externa | no se puede determinar ]

6. ¿Cuál es el factor de forma de esta unidad?
   [ 6 Gb/s | 1 TB | 3.5 pulgadas | 7,200 RPM | 32 MB ]

7. ¿Cuántos otros dispositivos podrían estar en el mismo cable que conecta este dispositivo a la placa madre?
   [ 0 | 1 | 2 | 3 | no se puede determinar ]

8. Si solo hay dos unidades disponibles, ¿qué niveles de RAID se pueden usar? (Elige todos los que correspondan.)
   [ 0 | 1 | 5 | 10 ]

9. Se ha llamado a un técnico para que ayude con un problema. Aparece un error de S.M.A.R.T. y el usuario informa que el sistema ha estado funcionando lentamente durante varios meses. ¿Qué dos herramientas o acciones debería usar el técnico de inmediato?
   [ chkdsk | particionar la unidad | aplicar formato de alto nivel a la unidad | convert | diskpart | respaldar los datos | conectar unidades externas y configurar Espacios de almacenamiento ]

10. ¿Cuál es la diferencia entre distribuir (spanning) y seccionar (striping)?
    a. La distribución se hace en hardware y el seccionado en software.
    b. La distribución se hace dentro de RAID y el seccionado en Windows o a través de la BIOS/UEFI.
    c. La distribución toma dos unidades y el seccionado toma tres unidades.
    d. La distribución llena una unidad antes de pasar a la siguiente, mientras que el seccionado alterna entre las unidades.
    e. La distribución es RAID 0 y el seccionado es RAID 1.

11. Un almacén de baldosas y alfombras usa varias computadoras para el proceso de inventario. Las computadoras del área del almacén tienen una tasa de fallo de disco duro más alta que las del área de oficina. ¿Qué solución ayudará a esta empresa?
    a. Reemplazar los discos duros por SSD.
    b. Colocar alfombrillas antiestáticas debajo de las computadoras y en el suelo donde las personas se paran o se sientan para usar la computadora.
    c. Instalar fuentes de alimentación más potentes.
    d. Instalar ventiladores de CPU adicionales.
    e. Reemplazar las unidades por unidades de mayor RPM.

Un usuario quiere añadir una SSD a una computadora. Considera las siguientes especificaciones de la SSD que se está comprando y la documentación de la placa madre del usuario al responder las preguntas 12 a 16.

Especificaciones:

- Capacidad de 1 TB
- Interfaz PCIe 3.0 x4
- M.2 2280

Documentación de la placa madre:

- 1 x zócalo M.2_1 3 con muesca M, compatible con dispositivos de almacenamiento tipo 2242/2260/2280/22110 (modo SATA y PCIe 3.0 x4)
- 1 x zócalo M.2_2 3 con muesca M, compatible con dispositivos de almacenamiento tipo 2242/2260/2280/22110 (modo SATA y PCIe 4.0 x4)

12. ¿Esta unidad es interna o externa? ¿Cómo puedes saberlo?
    [ interna | externa ]

13. ¿Se podrá instalar la SSD en la computadora según las especificaciones dadas?
    [ Sí | No | No se puede determinar con la información proporcionada ]

14. Al considerar la documentación de la placa madre, ¿qué significan los números 2242/2260/2280/22110?

15. ¿Cuál es un inconveniente de las SSD?
    [ tiempo de instalación | MTBF | requisitos de mantenimiento | costo | velocidad | confiabilidad ]

16. ¿Funcionaría la SSD en el zócalo M.2_2?
    [ Sí | No | No se puede determinar con la información proporcionada ]

17. ¿Qué herramienta usan la mayoría de los usuarios de Windows para comprobar si hay clústeres perdidos?
    [ comprobación de errores (Comprobar/Comprobar ahora) | diskpart | Desfragmentador de disco | Liberador de espacio en disco ]

18. ¿Cómo usaría un técnico el LED de la unidad para solucionar problemas de un disco duro?

19. [ V | F ] Si tienes suficiente RAM instalada, el disco duro no se usará como memoria caché.

20. Estás hablando por teléfono con un cliente que está molesto. El cliente insulta y comienza a gritar. ¿Qué debes hacer?
    a. Colgar al interlocutor.
    b. Preguntar al interlocutor si puedes ponerla en espera mientras se calma.
    c. Hablar con el cliente usando un tono tranquilo y profesional.
    d. Mantener la calma pero subir un poco el volumen de tu voz para mostrar la importancia y el profesionalismo de tu respuesta técnica.

## Ejercicios

### Ejercicio 7.1 Planificar la instalación y configuración de dispositivos de almacenamiento

**Objetivo:** ser capaz de usar la documentación de la placa madre para planificar varios escenarios de dispositivos de almacenamiento.

**Procedimiento:** consulta la siguiente figura y responde las preguntas correspondientes.

**Preguntas:** consulta la Figura 7.51 para responder las preguntas 1 a 10.

> Figura 7.51 Documentación del Ejercicio 7.1

1. Un usuario tiene la placa madre mostrada y quiere instalar dos discos duros internos. Usando la Figura 7.51, determina qué puertos debería usar para conectar los discos duros. (Enumera dos.)
2. Ahora el usuario quiere añadir una tercera unidad, una SSD interna. Enumera todos los puertos que el usuario podría usar que aún no se hayan usado.
3. Si el usuario está considerando una SSD externa y quiere usar eSATA, ¿cómo conectaría los cables a esta placa madre que no tiene un puerto eSATA?
4. ¿Cuál es el significado de los números 2242, 2260, 2280 y 22110 en la placa madre?
5. ¿Se podría usar cualquiera de las ranuras M.2 para un disco duro mecánico interno?
   [ Sí | No ]
6. ¿Se podría usar cualquiera de las ranuras M.2 para una SSD interna?
   [ Sí | No ]
7. Si la documentación de la placa madre indica que se admite una SSD NVMe, ¿qué puertos/ranuras se podrían usar?
8. ¿Cuál es el número máximo de discos duros mecánicos que se podrían instalar usando esta placa madre? ¿Cómo determinaste el número máximo?
9. ¿Qué puertos externos se podrían usar para un disco duro mecánico externo? Enumera todos los que correspondan.
10. ¿Qué puertos externos se podrían usar para una SSD externa? Enumera todos los que correspondan.

### Ejercicio 7.2 Configurar un disco duro SATA en papel

**Objetivo:** ser capaz de configurar los puentes de un disco duro SATA.

**Partes:** computadora con acceso a internet.

**Procedimiento:** consulta las siguientes figuras y responde las preguntas correspondientes.

**Preguntas:** consulta la Figura 7.52 para responder las preguntas 1 a 3.

> Figura 7.52 Documentación del Ejercicio 7.2, parte 1

1. Considerando la información proporcionada, ¿cuándo cambiarías los puentes de esta unidad?
2. Si la unidad tiene los pines 1 y 2 puenteados, ¿qué versión de SATA está usando la unidad?
   [ SATA 1 | SATA 2 | SATA 3 ]
3. Si este disco duro se instalara en un modelo de escritorio, ¿cuál sería el factor de forma de esta unidad muy probablemente?
4. Consulta la Figura 7.53. La información proporcionada es para una computadora portátil usada en un entorno empresarial. ¿Cuáles crees que serían los efectos de instalar un puente en los pines 1 y 2 de esta unidad?

> Figura 7.53 Documentación del Ejercicio 7.2, parte 2

5. Usa internet para determinar la configuración de los puentes SATA de un disco duro de reemplazo de un proveedor en particular. Escribe la configuración de los puentes y la explicación de los mismos. Escribe la URL donde encontraste esta información.
6. ¿Cuál es el factor de forma del disco duro al que se hace referencia en la pregunta 5?

## Actividades

### Descubrimiento en internet

**Objetivo:** usar internet para obtener información específica sobre una computadora o sus partes asociadas.

**Partes:** computadora con acceso a internet.

**Preguntas:** usa internet para responder las siguientes preguntas. Escribe las respuestas y la URL del sitio donde encontraste la información de cada respuesta. Al responder las preguntas 1 a 3, supón que acabas de comprar un disco duro Seagate Barracuda de 3 TB, 7,200 RPM y 6 Gb/s.

1. ¿Qué tipos de cables se necesitan para esta unidad? ¿Vienen con la unidad? Escribe las respuestas y la URL donde encontraste esta información.
2. ¿Cuánta caché tiene esta unidad?
3. Si la computadora no tiene un conector SATA disponible, ¿qué recomendación podrías hacer?
4. Un cliente tiene una SSD interna Western Digital WD Blue SN550 NVMe M.2 de 500 GB NAND 3D. ¿Cuál es la versión mínima de PCIe necesaria para instalar esta tarjeta? Enumera el sitio web donde encontraste esta respuesta.
   [ 1 | 2 | 3 | 4 ]
5. Basándote en la misma unidad de la pregunta 4 y en la información que aprendiste en este capítulo, ¿qué tamaño de ranura debe admitir la placa madre para poder instalar esta unidad?
   [ 550 | 5502 | 2400 | 2280 | 22110 ]
6. Encuentra un disco duro eSATA y un disco duro SATA interno que sean iguales o de capacidad cercana. ¿Cuál es la diferencia de precio entre los dos? Escribe la respuesta y la URL donde encontraste esta información.

Mira el video «How to use all capacities of a new hard drive over 2TB? DFI knowledgebase», en https://us.dfi.com/knowledge/video/17, para responder las preguntas 7 a 10. (Si este enlace no funciona cuando intentes usarlo, busca un video que muestre cómo instalar una partición GPT o busca este video en youtube.com).

7. ¿Qué herramienta de Windows se usó para convertir la partición en una partición GPT? [ Administrador de tareas | Administración de discos | Administrador de dispositivos | símbolo del sistema ]
8. Aunque la unidad Disco 1 originalmente no estaba particionada, antes de que el presentador hiciera algo con la unidad, la unidad se mostró como si tuviera cuántas secciones no asignadas. [ 1 | 2 | 3 ]
9. Si una unidad ya ha sido particionada y tiene datos, ¿qué debes hacer antes de convertir la unidad en un disco GPT?
10. Enumera un comentario que encontraste interesante e informativo.

### Habilidades interpersonales

**Objetivo:** mejorar y afinar la capacidad de un técnico para escuchar, comunicarse de forma escrita y oral, y apoyar a las personas que usan computadoras de manera profesional.

**Actividades:**

1. En grupos de dos, finjan que uno de ustedes tiene un problema de disco duro. El otro estudiante debe pretender ayudarlo por teléfono. Comparte tu conversación telefónica con otros dos grupos. Selecciona el mejor grupo y escenario.
2. Con otros dos compañeros de clase, propongan 10 consejos adicionales para un buen soporte telefónico que no se hayan enumerado en el capítulo. Comparte tus ideas con la clase.
3. Como equipo, planifiquen la instalación de tres dispositivos de almacenamiento. El dispositivo de arranque será una SSD SATA con una SSD interna mecánica usada para el almacenamiento de datos, así como una unidad mecánica USB externa. En tu plan, detalla qué unidades estás usando para el plan, qué cosas comprobarás, cómo obtendrás la documentación y qué obstáculos podrían aparecer como parte del proceso de instalación. El usuario también querría algún tipo de redundancia. ¿Qué opciones podrías presentarle al usuario? Comparte tu plan con otros equipos.

### Habilidades de pensamiento crítico

**Objetivo:** analizar y evaluar información, así como aplicar la información aprendida a situaciones nuevas o diferentes.

**Actividades:**

1. Enumera tres cosas que podrían hacer que una computadora se bloquee periódicamente y que estén relacionadas con el disco duro. ¿Qué podrías hacer para corregir, comprobar o verificar estas tres cosas?
2. Un cliente quiere actualizar o reemplazar su disco duro. Repasa los pasos que seguirías de principio a fin para realizar esta tarea.
3. Tu equipo da soporte a un departamento con 20 estaciones de trabajo. Algunas personas almacenan información muy importante en sus discos duros locales. Usa internet para investigar opciones de redundancia, así como las opciones presentadas en el capítulo. Desarrolla una lista de posibles planes de redundancia para el departamento.
