# Capítulo 5. Desmontaje y energía

> Traducción al español del Capítulo 5 («Disassembly and Power») de *Complete A+ Guide to IT Hardware and Software: CompTIA A+ Exams 220-1101 & 220-1102* (Cheryl A. Schmidt, Christopher Lee) — material de estudio de uso personal.
>
> Nota: las figuras del libro son imágenes y no se incluyen aquí; se conserva su leyenda traducida como referencia. Las tablas se transcriben como tablas de Markdown.

En este capítulo aprenderás:

- Cómo evitar que la electricidad estática, la RFI y la EMI dañen o interfieran con una computadora
- Las herramientas necesarias para trabajar en computadoras
- Cómo desarmar una computadora y volver a armarla
- Cómo realizar comprobaciones básicas de voltaje y continuidad
- Cómo instalar, actualizar o reemplazar una fuente de alimentación
- Consejos para una buena comunicación escrita

**Objetivos del examen CompTIA:**

- 1101-3.1 Explicar los tipos básicos de cable y sus conectores, características y propósitos.
- 1101-3.4 Dado un escenario, instalar y configurar placas madre, unidades centrales de procesamiento (CPU) y tarjetas adicionales.
- 1101-3.5 Dado un escenario, instalar o reemplazar la fuente de alimentación adecuada.
- 1101-5.2 Dado un escenario, diagnosticar problemas comunes relacionados con placas madre, RAM, CPU y energía.
- 1102-4.4 Dado un escenario, usar procedimientos de seguridad comunes.
- 1102-4.5 Resumir los impactos ambientales y los controles ambientales locales.
- 1102-4.7 Dado un escenario, usar técnicas de comunicación y profesionalismo adecuadas.

## Descripción general del desmontaje

Rara vez es necesario desmontar por completo una computadora. Sin embargo, cuando un técnico recién está aprendiendo sobre las PC, el desmontaje puede ser tanto informativo como divertido. Un técnico podría desmontar una computadora cuando tiene un problema de causa indeterminada o un problema de conexión a tierra. Un **problema de conexión a tierra** del equipo ocurre cuando la placa madre o el adaptador no está instalado correctamente y una pista (una línea de metal en la placa madre o el adaptador) toca el chasis de la computadora, lo que hace que el adaptador y posiblemente otros componentes dejen de funcionar.

## Descarga electrostática (ESD)

Debes tomar precauciones al desmontar una computadora. Los circuitos electrónicos ubicados en la placa madre y en los adaptadores están sujetos a la ESD. La **descarga electrostática (ESD)** es una diferencia de potencial entre dos elementos que provoca electricidad estática. La electricidad estática puede dañar el equipo electrónico. La persona promedio no puede sentir una descarga estática hasta que alcanza los 3000 volts. Un componente electrónico puede dañarse con tan solo 30 volts. Es posible que algunos componentes electrónicos no se dañen la primera vez que ocurre la electricidad estática. Sin embargo, los efectos de la electricidad estática pueden ser acumulativos, debilitando o eventualmente destruyendo un componente. Un evento de ESD no es recuperable: no se puede hacer nada respecto del daño que indujo. Los chips electrónicos y los módulos de memoria son los más susceptibles a los impactos de ESD.

### Consejo técnico: las condiciones atmosféricas afectan la electricidad estática

Cuando la humedad es baja, el potencial de ESD es mayor que en cualquier otro momento; sin embargo, demasiada humedad es mala para la electrónica. Mantén la humedad entre el 45 % y el 55 % para reducir la amenaza de ESD.

Un técnico puede prevenir la ESD usando una variedad de métodos. La táctica más común es usar una **pulsera antiestática**, también llamada **correa ESD**. Una pulsera antiestática permite que un técnico y una computadora estén al mismo potencial de voltaje. Mientras el técnico y la computadora o la pieza electrónica estén al mismo potencial, no se produce electricidad estática. Ver la Figura 5.1.

> Figura 5.1 Pulsera antiestática

Un extremo rodea la muñeca del técnico y el otro extremo se sujeta a la computadora. El clip se sujeta a un poste de conexión a tierra o a una parte metálica, como la fuente de alimentación o el chasis, como se muestra en la Figura 5.2. Es posible que veas el símbolo electrónico de tierra, ⏚, cerca de un poste de tierra.

> Figura 5.2 Dónde sujetar una pulsera antiestática

### Consejo técnico: cuándo no usar una pulsera antiestática

Los técnicos no deben usar una correa de muñeca ESD cuando trabajan dentro de un monitor de tubo de rayos catódicos (CRT) o de una fuente de alimentación, debido a los altos voltajes que hay allí. Por supuesto, un técnico no debería estar dentro de estos dispositivos a menos que esté debidamente capacitado en electrónica.

Se pueden usar **guantes antiestáticos** (ver la Figura 5.3) en lugar de una pulsera antiestática. Las laptops y otros dispositivos móviles con frecuencia no tienen buenos lugares para sujetar una pulsera y, en tal caso, los guantes antiestáticos funcionan mejor.

> Figura 5.3 Guantes antiestáticos

Las **bolsas antiestáticas** son buenas para almacenar adaptadores y placas madre de repuesto cuando las piezas no están en uso. Sin embargo, las bolsas antiestáticas pierden su eficacia después de unos años. La Figura 5.4 muestra una bolsa antiestática con un adaptador dentro. Hay **tapetes ESD** disponibles para colocar debajo de una computadora que se está reparando, y dicho tapete puede tener un broche para conectar una pulsera antiestática.

> Figura 5.4 Bolsa antiestática

Si no hay disponible una pulsera antiestática, aún puedes reducir la posibilidad de daño por ESD. Después de quitar la cubierta de la computadora, mantente en contacto con una parte metálica no pintada de la computadora, como la fuente de alimentación. Retira las piezas de la computadora una por una, manteniendo siempre el codo (o alguna otra parte descubierta del brazo) tocando la fuente de alimentación. Este método de **autoconexión a tierra** es una forma eficaz de mantener a un técnico y a una computadora al mismo potencial de voltaje, reduciendo así la posibilidad de daño por ESD. Sin embargo, no es tan seguro como usar una pulsera antiestática. Además, retira el cable de alimentación de la parte trasera de la computadora porque una fuente de alimentación proporciona una pequeña cantidad de energía a la placa madre incluso cuando la computadora está apagada. ¡Siempre desenchufa la computadora y usa una pulsera antiestática cuando retires o reemplaces piezas dentro de una computadora!

### Consejo técnico: buenas noticias sobre la ESD

Los fabricantes de electrónica están diseñando componentes menos susceptibles a la ESD. Sin embargo, aún debes conectarte a tierra usando cualquier medio posible. ¡Cada descarga debilita un componente!

## Interferencia electromagnética (EMI)

La **interferencia electromagnética (EMI)** es el ruido causado por dispositivos eléctricos, como una computadora, un sacapuntas eléctrico, un motor, una aspiradora, un aire acondicionado y la iluminación fluorescente. Los dispositivos eléctricos alrededor del chasis de la computadora, incluidos los altavoces, causan más problemas de EMI que la propia computadora.

Un tipo específico de interferencia electromagnética que afecta negativamente a las computadoras es la **interferencia de radiofrecuencia (RFI)**. La RFI son simplemente ruidos que ocurren en el rango de radiofrecuencia. Si una computadora tiene un problema intermitente, revisa los dispositivos circundantes para encontrar la fuente de ese problema. Los problemas de EMI son muy difíciles de rastrear hasta su origen. Cualquier dispositivo electrónico, incluidas las computadoras e impresoras, puede ser una fuente de EMI o RFI. La EMI también puede llegar a través de las líneas eléctricas. Mueve la computadora a un tomacorriente diferente o a un circuito totalmente distinto para determinar si el tomacorriente es la fuente del problema. La EMI también puede afectar los archivos de un disco duro.

### Consejo técnico: reemplazar las tapas de ranura vacías

Para ayudar con los problemas de EMI y RFI, vuelve a colocar las tapas de ranura para las ranuras de expansión que ya no se usan. Las tapas de ranura se muestran en la Figura 4.13 (consulta el Capítulo 4, «Introducción a la configuración»). Las tapas de ranura también evitan el polvo y mejoran el flujo de aire dentro del chasis.

## Herramientas

Ningún capítulo sobre desmontaje y reensamblaje estaría completo sin mencionar las herramientas. Las herramientas se usan para retirar/reemplazar unidades reemplazables en campo (FRU), que son partes de la computadora u otros dispositivos electrónicos, como la fuente de alimentación o la placa madre.

Muchos técnicos no van a una visita de reparación con un maletín de herramientas completo. La gran mayoría de todas las reparaciones se completan con las siguientes herramientas básicas que se muestran en la Figura 5.5:

> Figura 5.5 Herramientas básicas del técnico de PC

- Destornilladores de punta plana pequeños y medianos
- Destornilladores Phillips n.º 0, n.º 1 y n.º 2
- Llaves de tuercas hexagonales de 1/4 y 3/16 de pulgada
- Alicates de corte diagonal pequeños
- Alicates de punta larga (pinza de puntas)

Los destornilladores se encargan de la mayoría de los desmontajes y reensamblajes. A veces los fabricantes colocan bridas (amarres) en piezas nuevas, cables nuevos o los cables dentro del chasis de la computadora. Los alicates de corte diagonal son excelentes para quitar estas bridas sin cortar los cables ni dañar las piezas. Los alicates de punta larga son buenos para enderezar pines doblados en cables o conectores, y son útiles para un millón de otras cosas. Los destornilladores pequeños de precisión y los alicates de punta larga son indispensables.

### Consejo técnico: recuperar esos tornillos rebeldes

Los destornilladores magnéticos son prácticos para recoger tornillos caídos. Sin embargo, pueden afectar la memoria, así que evita usarlos si es posible. Si un tornillo rueda debajo de la placa madre y no se puede alcanzar, inclina la computadora para que el tornillo ruede hacia afuera. A veces hay que inclinar el chasis en diferentes direcciones hasta que el tornillo se desprenda.

## Desmontaje

Antes de que un técnico desmonte una computadora, deben considerarse los siguientes pasos de desmontaje:

- No retires la batería de la placa madre; si lo haces, se perderá la información de configuración del CMOS.
- Usa procedimientos de conexión a tierra adecuados para evitar daños por ESD.
- Ten papel, un bolígrafo, un teléfono o una cámara digital cerca para tomar notas, hacer diagramas y tomar fotos. Aunque hayas desarmado computadoras durante años, puedes encontrar algo único o diferente dentro de esta.
- Ten un espacio de trabajo amplio, plano y limpio.
- Al retirar adaptadores, no apiles los adaptadores uno sobre otro.
- Si es posible, coloca los adaptadores retirados dentro de una bolsa protectora ESD especial.
- Maneja cada adaptador, placa madre o procesador por los bordes laterales. Evita tocar los contactos dorados en la parte inferior de los adaptadores. El sudor, el aceite y la suciedad causan problemas.
- Recuerda que los discos duros requieren un manejo cuidadoso. Un golpe muy pequeño puede dañar los datos almacenados.
- Puedes retirar una fuente de alimentación, pero no la desmontes sin la capacitación y las herramientas adecuadas.
- Documenta las ubicaciones de tornillos y cables. Etiquétalos si es posible.

La siguiente sección describe los pasos para desmontar una computadora.

### Paso 1. Retirar la energía y los cables externos

El primer paso al desmontar una computadora es retirar el cable de alimentación. Se envía una pequeña cantidad de energía a la placa madre incluso cuando la computadora está apagada, de modo que la computadora pueda "despertarse" en un entorno corporativo y se puedan aplicar actualizaciones. Lo siguiente es retirar los cables externos. Toma notas sobre qué cable se conecta a cada puerto específico. La Figura 5.6 muestra la parte trasera de la computadora, donde se hace esto.

> Figura 5.6 Retirar la energía y los cables externos

### Paso 2. Abrir el chasis

Abrir o retirar el chasis es a veces la parte más difícil del desmontaje. Algunos fabricantes tienen lengüetas o cubiertas sobre los tornillos de retención, y otros tienen palancas o lengüetas de retención que deben presionarse antes de que la cubierta se deslice para abrirse o separarse. En algunas computadoras, debes presionar hacia abajo una lengüeta en la parte superior de la computadora mientras presionas simultáneamente hacia arriba una lengüeta en la parte inferior de la computadora. Una vez que se presionan las lengüetas, se puede hacer palanca para abrir la cubierta. Algunos chasis tienen tornillos que se aflojan pero que no tienen que retirarse por completo para quitar o abrir el chasis. Para todos los tornillos de la computadora, haz diagramas y coloca los tornillos en una huevera con cada sección de la huevera etiquetada con el lugar de donde tomaste los tornillos. Recuerda que para retirar o aflojar un tornillo, gira el destornillador hacia la izquierda. Cuando sea posible, consulta las instrucciones del fabricante al abrir un chasis. La mayoría de las veces, puedes acceder al interior de la computadora simplemente retirando los tornillos que sujetan el panel lateral, como se muestra en la Figura 5.7.

> Figura 5.7 Retirar los tornillos del chasis

### Paso 3. Retirar los cables y conectores internos

Los cables internos comúnmente conectan un dispositivo a la placa madre, la fuente de alimentación a un dispositivo, la placa madre a los botones o puertos del panel frontal, y/o desde una tarjeta que ocupa un espacio de expansión hasta un dispositivo. Los cables pueden ser complicados. Insertar un cable al revés en un dispositivo o un adaptador puede dañar el dispositivo, la placa madre o el adaptador. La mayoría de los cables tienen una muesca de manera que el cable se inserta de una sola forma en el conector. Sin embargo, algunos cables o conectores no tienen muesca. Algunos cables tienen una lengüeta de tracción o una pieza de plástico que se usa para retirar el cable del conector y/o del dispositivo. Úsala si es posible o sujeta firmemente el conector, no el cable. Si un conector tiene una lengüeta de bloqueo, libera la lengüeta antes de desconectar el cable para evitar dañar el cable y/o el conector.

Ten cuidado con los cables de las unidades. Algunos de los cables estrechos de las unidades, como los cables Serial Advanced Technology Attachment (SATA), no son muy robustos y no se conectan con tanta firmeza como algunos de los otros cables de la computadora. Además, con este tipo particular de cable, no importa qué extremo del cable se conecte al dispositivo. Una versión en ángulo de 90° de este cable (ver la Figura 5.8) podría conectarse a dispositivos en un chasis de diseño de espacio limitado y podría tener un pestillo de liberación.

> Figura 5.8 Cables SATA, incluido el cable en ángulo de 90° con pestillo a la derecha

### Consejo técnico: conexiones firmes

Al conectar cables a una placa madre o a componentes internos, asegúrate de que cada cable esté conectado firmemente, de manera uniforme y segura.

Por lo general, los conectores de la placa madre tienen muescas de manera que el cable se inserta de una sola forma; sin embargo, no todos los cables tienen muescas. Algunas placas madre tienen el pin 1 (o el pin opuesto) etiquetado. Consulta siempre la documentación de la placa madre para la orientación correcta de un cable en un conector de la placa madre.

Cada cable tiene un cierto número de pines, y todos los cables tienen un pin 1. El pin 1 de un cable se conecta al pin 1 de un conector. El conector del cable generalmente tiene una flecha grabada en su molde que muestra la conexión del pin 1. La Figura 5.9 muestra el pin 1 en un cable Internal Drive Electronics (IDE).

> Figura 5.9 Pin 1 en un cable plano IDE PATA de 40 pines

La Figura 5.10 muestra los conectores SATA usados para los cables de la Figura 5.8 que se conectan a discos duros y/o unidades ópticas. Estos conectores comúnmente tienen discos duros y/o unidades ópticas conectados. La Figura 5.11 muestra otros dos conectores de la placa madre: el conector superior es un conector IDE para unidades Parallel ATA (PATA) más antiguas, y el inferior es para la alimentación de la placa madre. Observa que el conector superior tiene una muesca (abertura). Observa también que el conector inferior tiene ciertas aberturas de conector que son diferentes de las cuadradas para evitar insertar el cable en la dirección incorrecta.

> Figura 5.10 Conectores SATA de unidad en la placa madre

> Figura 5.11 Dos conectores de placa madre (IDE más antiguo arriba y alimentación de placa madre abajo)

Cables específicos se conectan desde los conectores del panel frontal de la placa madre hasta luces, puertos o botones del panel frontal. Estos incluyen el botón de encendido, un botón de reinicio, puertos USB, un puerto de micrófono, un puerto de auriculares, altavoces, ventiladores, la luz de actividad de la unidad y la luz de encendido, por nombrar algunos. Ten mucho cuidado al retirar y reinstalar estos cables. Por lo general, cada uno de ellos tiene un conector que debe sujetarse a los pines correspondientes de la placa madre. Asegúrate de revisar todos los puertos y botones después de haber reconectado estos cables. Consulta la documentación de la placa madre si tus diagramas, fotos o notas están incompletos. La Figura 5.12 muestra los pines de la placa madre y los cables.

> Figura 5.12 Cables del panel frontal de la placa madre

### Consejo técnico: conectar con cuidado los cables del panel frontal

Asegúrate de conectar los cables del panel frontal a los pines adecuados y en la dirección correcta. Algunos fabricantes etiquetan los cables. Como se muestra en la Figura 5.12, una vez que tienes uno orientado correctamente (por ejemplo, con las palabras hacia el exterior de la placa madre), los demás comúnmente se orientan en la misma dirección. Observa también en esta figura que todos los cables blancos se orientan en la misma dirección.

La placa madre también contiene pines que se usan para conectar cables como los que van a la CPU o a los ventiladores del chasis. Vuelve a mirar la Figura 3.24 (consulta el Capítulo 3, «En la placa madre») para ver cómo se conectan los ventiladores a los pines de la placa madre.

### Paso 4. Retirar los adaptadores

Los adaptadores comúnmente tienen tornillos de retención o una barra que mantiene los adaptadores firmemente en el chasis. (Consulta la Figura 4.13 del Capítulo 4 para ver una ilustración de estos dos métodos.) Usa los bordes del adaptador para tirar de él hacia arriba y sacarlo de la ranura de expansión. No toques los contactos en la parte inferior del adaptador. Nunca apiles adaptadores uno sobre otro. Si un adaptador no se va a reinstalar, inserta una cubierta en blanco de ranura de expansión en la ranura de expansión vacía para que se mantenga un flujo de aire adecuado dentro del chasis. La Figura 5.13 muestra un adaptador que se está retirando.

> Figura 5.13 Retiro de un adaptador

### Paso 5. Retirar los dispositivos de almacenamiento

Los discos duros deben manejarse con cuidado al desmontar una computadora. Dentro de los discos duros mecánicos tradicionales hay platos duros con cabezas de lectura/escritura diminutas ubicadas a solo milímetros por encima de los platos. Si se caen, las cabezas de lectura/escritura podrían tocar el plato, causando daño al plato y/o a las cabezas de lectura/escritura. El plato contiene los datos y las aplicaciones. Los discos duros mecánicos actuales tienen cabezas de autoestacionamiento que alejan las cabezas hacia un área segura cuando la computadora está apagada o en un modo de ahorro de energía. Incluso con cabezas de autoestacionamiento, el manejo inadecuado puede causar daño al disco duro.

Una **unidad de estado sólido (SSD)** no contiene cabezas frágiles. Sin embargo, estas unidades son susceptibles a la ESD. Usa procedimientos de manejo antiestático adecuados al retirarlas/instalarlas. Guarda una unidad de estado sólido en una bolsa antiestática cuando no esté en uso.

Una unidad se desliza dentro de una bahía de unidades. Algunos chasis requieren que la unidad tenga rieles que se sujeten a los lados de la unidad. Otros chasis requieren que la unidad se atornille en la bahía del disco duro. La Figura 5.14 muestra un disco duro que se está retirando. Puedes ver que este chasis en particular requiere tornillos para asegurar las unidades insertadas en las bahías de unidades.

> Figura 5.14 Retirar un disco duro

La Figura 5.15 muestra un disco duro que tiene un riel guía sujeto y un conjunto diferente de rieles guía debajo de la unidad. Al reemplazar una unidad, los rieles de la unidad tendrían que retirarse de la unidad antigua y sujetarse a la unidad de reemplazo. Al instalar una unidad nueva, es posible que haya que comprar los rieles de la unidad.

> Figura 5.15 Rieles de disco duro

### Paso 6. Retirar la placa madre

El Capítulo 3 cubre el reemplazo de la placa madre ampliamente, así que aquí analizamos cuestiones relacionadas con construir una computadora desde cero o desmontar una computadora. Algunos chasis incluyen un escudo de panel de E/S estándar que podría necesitar retirarse para instalar el escudo de E/S que viene con algunas placas madre. El **escudo de E/S** es una pieza que permite un flujo de aire y una conexión a tierra óptimos para los puertos de la placa madre. El escudo de E/S ayuda a garantizar que la placa madre esté instalada correctamente y alineada adecuadamente con el chasis. La Figura 5.16 muestra un escudo de E/S de placa madre.

> Figura 5.16 Escudo de E/S de la placa madre

Algunos chasis de computadora tienen separadores de plástico o metal (comúnmente de latón) que permiten atornillar la placa madre en el chasis sin que las soldaduras de la placa madre toquen y se conecten a tierra con el chasis de la computadora, lo que haría que la placa madre no funcione. Algunos separadores son de plástico y se deslizan en las ranuras del chasis de la computadora. No retires este tipo de separadores; simplemente déjalos sujetos y desliza la placa madre fuera de las ranuras. Un tipo de separador metálico se atornilla en el chasis; este separador tiene un lado roscado sobre el que se asienta la placa madre y un tornillo que sujeta la placa madre al separador, como se muestra en la Figura 5.17.

> Figura 5.17 Separador (standoff) de la placa madre

Algunas placas madre no solo tienen tornillos que las sujetan a los separadores metálicos, sino también uno o más clips de retención. Es posible que haya que presionar hacia abajo, levantar o doblar hacia arriba un clip de retención para poder deslizar la placa madre fuera del chasis. El chasis podría contener una o más muescas, y es posible que haya que deslizar la placa madre en una dirección particular (por lo general, en la dirección que va en sentido contrario a los puertos de E/S traseros) antes de levantarla del chasis.

### Computadoras todo-en-uno

Los mismos conceptos de desmontaje se aplican a las computadoras todo-en-uno que a las computadoras de escritorio en cuanto al cableado, el retiro de dispositivos de almacenamiento, el retiro de RAM, el retiro de la placa madre y la energía. La diferencia es el espacio en el que se instalan los dispositivos: una computadora todo-en-uno tiene todo instalado en la parte trasera de la pantalla, como se muestra en la Figura 5.18.

> Figura 5.18 Partes de una computadora todo-en-uno

## Reensamblaje

Reensamblar una computadora es fácil si el técnico es cuidadoso y documenta adecuadamente el desmontaje. Tareas simples, como insertar la unidad óptica en la bahía de unidades correcta, se vuelven confusas después de retirar muchas piezas. Escribir recordatorios o tomar fotos toma menos tiempo que tener que diagnosticar una computadora debido a un mal reensamblaje. Un técnico debe volver a insertar todos los componentes en sus lugares correctos, teniendo cuidado de reemplazar todos los tornillos y piezas e instalar las cubiertas de ranura faltantes, si es posible.

Al reinstalar una placa madre, invierte el procedimiento usado durante el desmontaje. Asegúrate de que la placa madre esté asentada de forma segura en el chasis y de que se reemplacen todos los clips de retención y/o tornillos. La inspección visual también puede ayudar. Asegúrate de que los puertos se extiendan completamente desde el chasis a través del escudo de E/S. Como paso final, asegúrate de que las unidades y la cubierta estén alineadas correctamente cuando se reinstale el chasis.

Los cables y conectores son las fuentes más comunes de problemas de reensamblaje una vez que la placa madre está instalada. Asegúrate de que los cables estén completamente sujetos a los dispositivos y al mismo conector de la placa madre. Asegúrate de que los cables de alimentación estén firmemente sujetos.

## Mantenimiento preventivo

En el curso del uso diario, las computadoras se ensucian (ver la Figura 5.19), especialmente por dentro. Se acumula el polvo, creando así aislamiento y aumentando la cantidad de calor generado. El calor adicional puede hacer que los componentes electrónicos se sobrecalienten y fallen. También puede hacer que el procesador funcione de manera constante a una velocidad más baja. El polvo es un enemigo de las computadoras.

> Figura 5.19 Polvo dentro de un compartimento

El **mantenimiento preventivo** incluye ciertos procedimientos realizados para prolongar la vida de una computadora. Una computadora en un entorno de trabajo normal debe limpiarse al menos una vez al año. Las medidas preventivas típicas incluyen aspirar la computadora y limpiar el láser de la unidad óptica, las teclas del teclado, la impresora y la pantalla de visualización. Asegúrate de apagar una computadora y retirar el cable de alimentación, retirar la batería y el adaptador de CA de una laptop u otro dispositivo móvil, y permitir que una impresora láser se enfríe antes de acceder a las piezas internas. Las medidas preventivas para muchos dispositivos individuales se describen en sus respectivos capítulos. Por ejemplo, los pasos que detallan cómo limpiar discos ópticos se incluyen en el Capítulo 8, «Dispositivos multimedia». Esta sección da una descripción general de un programa de mantenimiento preventivo y algunos consejos generales sobre la limpieza de solventes.

### Consejo técnico: limpiar con cuidado los monitores LCD y las pantallas de laptop

Usa uno de los siguientes elementos para limpiar monitores LCD y pantallas de laptop: (1) toallitas diseñadas específicamente para LCD o (2) un paño suave sin pelusa humedecido con agua o con una mezcla de alcohol isopropílico y agua. Nunca pongas líquido directamente sobre la pantalla y asegúrate de que la pantalla esté seca antes de cerrar la laptop.

Al realizar mantenimiento preventivo, enciende la computadora para asegurarte de que funcione. Realiza una inspección auditiva y visual de la computadora mientras arranca. Asegúrate de que la temperatura ambiente sea adecuada para el dispositivo. El equipo electrónico, como las PC y los dispositivos móviles, está diseñado para funcionar a temperatura ambiente (alrededor de 73 °F [23 °C]). Cualquier valor por encima de 80 °F (27 °C) debería justificar métodos de enfriamiento adicionales para el dispositivo.

Es una sensación terrible realizar mantenimiento preventivo en una computadora pero luego encenderla y descubrir que no funciona. Te preguntarás si la limpieza que realizaste causó el problema o si la computadora tenía un problema antes del mantenimiento preventivo.

A veces los fabricantes tienen un kit de mantenimiento preventivo para las visitas de servicio. El kit normalmente incluye los componentes enumerados y descritos en la Tabla 5.1.

> Tabla 5.1 Artículos de mantenimiento preventivo

| Artículo | Descripción |
|---|---|
| Aspiradora portátil | Se usa para aspirar la suciedad del interior de una computadora. Asegúrate de usar accesorios no metálicos. Con una aspiradora que tenga la capacidad de soplar aire, aspira primero y luego configura la aspiradora para que sople y saque el polvo de los lugares de difícil acceso. Sujeta las aspas del ventilador en su lugar mientras aspiras. |
| Aspiradora para tóner | Se usa para limpiar computadoras e impresoras láser. Se usan bolsas de aspiradora especiales para evitar que el tóner se derrita y potencialmente dañe la aspiradora. |
| Bolsas de aspiradora especiales | Se usan para impresoras láser para que el tóner no se derrita en el motor de la aspiradora. |
| Aire comprimido | Se usa para eliminar el polvo en lugares de difícil acceso (preferiblemente después de aspirar). |
| Hisopos de uretano | Se usan para limpiar entre las teclas de un teclado. Si una tecla se atasca, desconecta el teclado antes de rociar o usar limpiador de contactos en él. |
| Toallitas para monitor | Se usan en el frente de la pantalla. Las toallitas con una solución antiestática funcionan mejor. |
| Paños sin pelusa | Se usan para limpiar los touchpads de las laptops y otros componentes. Humedece el paño para eliminar los restos de grasa de los dedos. |
| Paños de uso general | Se usan para limpiar el exterior del chasis y limpiar las áreas del escritorio debajo y alrededor de una computadora. |
| Limpiador de uso general | Se usa con paños suaves sin pelusa o hisopos sin pelusa. Nunca rocíes ni viertas líquido sobre ninguna pieza de la computadora. |
| Alcohol desnaturalizado | Se usa en rodillos de goma, como los que están dentro de las impresoras. |
| Cepillo antiestático | Se usa para cepillar la suciedad de lugares de difícil acceso. |
| Kit de limpieza de unidad óptica | Puede incluir un limpiador de lentes que elimina el polvo y los residuos de una lente óptica; un limpiador de discos que elimina el polvo, la suciedad, las huellas dactilares y los aceites del disco; y un kit de reparación de rayones para restaurar, limpiar y pulir CD, DVD y BD. |
| Limpiador de contactos de oro | Se usa para limpiar los contactos de los adaptadores, así como los contactos de las baterías de laptop y los contactos donde se inserta la batería. |
| Gafas de seguridad | Se usan en entornos polvorientos o cuando se trabaja con sustancias químicas en un área mal ventilada. Las gafas con ventilación indirecta evitan que una salpicadura entre en contacto con los ojos. Las gafas sin ventilación protegen contra polvo, salpicaduras y vapores químicos. |
| Mascarilla de filtración de aire | Se usa para protegerse de vapores, polvo y humo transportados por el aire. Hay dos tipos de filtros: los de vapores y los de partículas. La filtración de vapores ayuda cuando se usan limpiadores y solventes químicos. La filtración de partículas ayuda con cosas que te hacen estornudar, como polvo, polen y moho. Inserta una capa adicional en la mascarilla para protección adicional. |

Una empresa de soluciones de limpieza puede proporcionar una hoja de datos de seguridad de materiales (MSDS) o una hoja de datos de seguridad (SDS) que contiene información sobre un producto, incluida su toxicidad, almacenamiento, eliminación y preocupaciones de salud/seguridad. Los componentes de la computadora tienen el potencial de contener sustancias tóxicas. Las empresas más grandes tienen reglas muy específicas sobre cómo se manejan los desechos electrónicos, pero tanto en empresas grandes como pequeñas, una persona de TI que trabaja con hardware necesita estar familiarizada con el manejo de desechos tóxicos. Cada estado comúnmente tiene procedimientos específicos de eliminación para solventes químicos y desechos tóxicos. Consulta con el coordinador de seguridad de la empresa para obtener información sobre el almacenamiento y la eliminación, usa la MSDS/SDS e investiga las pautas de manejo y eliminación de acuerdo con las regulaciones del gobierno local.

### Consejo técnico: conocer las leyes estatales sobre eliminación de aerosoles

Algunos estados tienen requisitos especiales para la eliminación de latas de aerosol, especialmente las que están obstruidas y aún contienen algo de producto. Cumple siempre con las regulaciones gubernamentales.

Para realizar el mantenimiento preventivo, apaga la computadora, retira el cable de alimentación y aspira la computadora con un accesorio no metálico. No comiences con aire comprimido ni soplando el polvo fuera de la computadora, porque la suciedad y el polvo simplemente irán al aire y eventualmente volverán a caer en la computadora y el equipo circundante. La Figura 5.20 muestra cómo aspirar el interior de una computadora. Recuerda sujetar con el dedo o un cepillo el aspa del ventilador para que no gire fuera de control y dañe el ventilador.

> Figura 5.20 Aspirado de mantenimiento preventivo

Después de aspirar todo lo posible, usa aire comprimido para soplar el polvo de los lugares de difícil acceso, como el interior de la fuente de alimentación y debajo de la placa madre (ver la Figura 5.21). Si estás realizando mantenimiento en una laptop, retira tantos módulos como sea posible antes de aspirar o usar aire comprimido. Informa a las personas en el área inmediata que quizás quieran salir del área si tienen alergias. Usa el equipo de seguridad adecuado, incluidas gafas de seguridad y una mascarilla, al realizar mantenimiento preventivo.

> Figura 5.21 Mantenimiento preventivo con aire comprimido

## Descripción general de electrónica básica

Un técnico necesita conocer algunos términos y conceptos electrónicos básicos al probar componentes. El mejor lugar para comenzar es con la electricidad. Hay dos tipos de electricidad: CA y CC. La electricidad proporcionada por un tomacorriente de pared es **corriente alterna (CA)**, y el tipo de electricidad usada por los componentes de la computadora es **corriente continua (CC)**. Dispositivos como radios, televisores y tostadoras usan energía de CA. Se usa energía de CC de bajo voltaje para los componentes internos de una computadora y para cualquier cosa alimentada por baterías. La fuente de alimentación de una computadora convierte la electricidad de CA del tomacorriente de pared a CC para los componentes internos. La electricidad implica electrones que fluyen a través de un conductor, de manera similar a como el agua corre por una tubería. Con la CA, los electrones fluyen alternadamente en ambas direcciones. Con la CC, los electrones fluyen en una sola dirección.

### Electrónica: terminología

Voltaje, corriente, potencia y resistencia son términos comúnmente usados en la industria de las computadoras. El **voltaje**, que es una medida de la presión que empuja los electrones a través de un circuito, se mide en volts y se muestra como un valor seguido de una V mayúscula. La salida de una fuente de alimentación se mide en volts. Las fuentes de alimentación típicamente emiten +3.3 volts, +5 volts, +12 volts y −12 volts. Comúnmente verás estos voltajes de salida mostrados en la documentación de la fuente de alimentación como +3.3V, +5V o +12V. Otra designación es +5VSB. Esta es para la energía en espera de la computadora, que siempre se proporciona, incluso cuando la computadora está apagada. Este voltaje suministrado es la razón por la que tienes que desenchufar una computadora cuando trabajas dentro de ella.

### Consejo técnico: la polaridad solo es importante al medir voltaje de CC

Cuando un técnico mide el voltaje proveniente de una fuente de alimentación, la punta negra del medidor (que es negativa) se conecta al cable negro de la fuente de alimentación (que es tierra). La punta roja del medidor se conecta a los cables de +5 o +12 volts de la fuente de alimentación.

El término volts también se usa para describir el voltaje de un tomacorriente de pared. El voltaje de un tomacorriente de pared normalmente es 120 VCA (120 volts de CA). Un **multímetro** es una herramienta que se usa para tomar lecturas de voltaje, como las de los conectores de la fuente de alimentación y los tomacorrientes de pared. La Figura 5.22 muestra un multímetro usado para tomar una lectura de voltaje de CC en los conectores de alimentación que salen de una fuente de alimentación. Cuando las puntas del medidor se insertan correctamente, el nivel de voltaje mostrado es de la polaridad correcta. Un multímetro también se puede usar para medir corriente (amperios) y resistencia (ohmios), que se analizan a continuación.

> Figura 5.22 Lectura de voltaje de CC

La lectura en el medidor podría ser la opuesta de lo que debería ser si las puntas del medidor están invertidas. La polaridad no es importante al medir CA. La Figura 5.23 muestra las reglas que se deben observar al trabajar con medidores.

> Figura 5.23 Reglas del medidor

Las fuentes de alimentación, las pantallas de panel plano y las pantallas de dispositivos móviles también contienen altos niveles de voltaje. Hay 120 volts de CA presentes dentro de la fuente de alimentación de una computadora de escritorio. Las fuentes de alimentación y los monitores tienen **capacitores** en su interior. Un capacitor es un componente que mantiene una carga incluso después de apagar la computadora.

La **corriente** se mide en amperios (amperes), que es el número de electrones que pasan a través de un circuito cada segundo. En la analogía de la tubería de agua, el voltaje es la cantidad de presión aplicada para forzar el agua a través de la tubería, y la corriente es la cantidad de agua que fluye. Cada dispositivo necesita una cierta cantidad de corriente para funcionar. Una fuente de alimentación está clasificada según la cantidad de corriente total (en amperios) que puede suministrar en cada nivel de voltaje. Por ejemplo, una fuente de alimentación podría estar clasificada a 20 amperios para el nivel de 5 volts y 8 amperios para el nivel de 12 volts.

La **potencia** se mide en vatios (watts), que es una medida de cuánto trabajo se está realizando. Se determina multiplicando volts por amperios. Las fuentes de alimentación se describen como que proporcionan un número máximo de vatios o que tienen una **clasificación de vataje** específica. Es la suma de todas las salidas (por ejemplo, [5 volts × 20 amperios] + [12V × 8 amperios] = 100 vatios + 96 vatios = 196 vatios).

### Consejo técnico: la corriente es lo que mata a las personas cuando se recibe una descarga eléctrica

El voltaje determina cuánta corriente fluye a través del cuerpo. Una situación de alta corriente y bajo voltaje es la más peligrosa.

La **resistencia** se mide en ohmios, que es la cantidad de oposición a la corriente en un circuito electrónico. El rango de resistencia de un medidor se puede usar para comprobar la continuidad o verificar si un fusible está en buen estado. Una comprobación de **continuidad** se usa para determinar si un cable tiene una rotura. Un conductor (cable) en un cable o un fusible en buen estado tendrá muy baja resistencia a la electricidad (cerca de 0 ohmios). Un cable roto o un fusible en mal estado tendrá una resistencia muy alta (millones de ohmios, a veces mostrada como ohmios infinitos, o OL). Por ejemplo, un cable normalmente está formado por varios alambres que van de un conector a otro. Si mides la continuidad de un extremo de un alambre al otro, debería mostrar ninguna resistencia. Si el alambre tiene una rotura, el medidor muestra resistencia infinita. La Figura 5.24 muestra ejemplos de una lectura de un cable en buen estado y una lectura de un cable roto.

> Figura 5.24 Lecturas de ejemplo de un medidor de resistencia

### Consejo técnico: desenchufa siempre una computadora antes de trabajar dentro de ella

La fuente de alimentación proporciona energía a la placa madre incluso si la computadora está apagada. Dejar el cable de alimentación conectado puede causar daños al reemplazar componentes como el procesador o la RAM.

Los medidores digitales tienen diferentes formas de mostrar el infinito. Consulta siempre el manual del medidor. Al comprobar la continuidad, el medidor se coloca en la configuración de ohmios, como se muestra en la Figura 5.24. La configuración de ohmios generalmente se ilustra con un símbolo omega (Ω).

### Consejo técnico: cómo manejar conexiones pequeñas con un medidor

Con conectores que tienen conexiones de pines pequeñas, usa una sonda de medidor delgada o inserta un alambre delgado, como un clip, en el orificio y toca el medidor con el alambre para tomar tu lectura.

La polaridad no es importante al realizar una comprobación de continuidad. Cualquiera de las puntas del medidor (roja o negra) se puede colocar en cualquiera de los extremos del alambre. Sin embargo, necesitas un diagrama de distribución de pines (lista de cableado) para el cable antes de poder comprobar la continuidad, porque el pin 1 de un extremo podría conectarse a un número de pin diferente en el otro extremo.

Un técnico necesita estar familiarizado con los términos y las comprobaciones electrónicas básicas. La Tabla 5.2 consolida esta información.

> Tabla 5.2 Términos básicos de electrónica

| Término | Valor | Uso |
|---|---|---|
| Voltaje | Volts | El voltaje es relevante al comprobar el voltaje de CA de un tomacorriente de pared (típicamente 120 VCA) y al comprobar el voltaje de salida de CC de una fuente de alimentación (típicamente +12, +3.3 y +5 VCC). |
| Corriente | Amperios (amperes) | Cada dispositivo necesita una cierta cantidad de corriente para funcionar. Una fuente de alimentación está clasificada para la corriente total en amperios de cada nivel de voltaje (por ejemplo, 24 amperios para energía de 5 volts y 50 amperios para energía de 12 volts). |
| Resistencia | Ohmios | La resistencia es la cantidad de oposición a la corriente eléctrica. Las mediciones de resistencia se usan para comprobar la continuidad de cables y fusibles. Un cable que muestra poca o ninguna resistencia no tiene roturas. Un fusible en buen estado no muestra resistencia. Si un cable tiene una rotura o si un fusible está en mal estado, la resistencia es infinita. |
| Vataje (potencia) | Watts | Los vatios son una medida de potencia y se derivan multiplicando amperios por volts. La salida de una fuente de alimentación se mide en vatios. |

## Descripción general de la fuente de alimentación

Una fuente de alimentación es un componente esencial dentro de una computadora; ningún componente/dispositivo interno de la computadora funciona sin ella. Una fuente de alimentación convierte CA a CC, distribuye energía de CC de bajo voltaje (voltaje de salida de 3.3V, 5V y 12V) a los componentes de toda la computadora y proporciona enfriamiento mediante el uso de un ventilador ubicado dentro de la fuente de alimentación. El voltaje de CA que acepta una fuente de alimentación normalmente es de 100 a 120 volts o de 200 a 240 volts. Ten en cuenta que los objetivos del examen de certificación A+ enumeran esto como **voltaje de entrada de 110V vs. 220V**. Algunas fuentes de alimentación de doble voltaje pueden aceptar cualquiera de los dos. Este tipo de fuente de alimentación puede tener un interruptor selector en la parte trasera o puede detectar automáticamente el nivel de voltaje de entrada.

Las fuentes de alimentación también pueden ser de conmutación automática. Una **fuente de alimentación de conmutación automática** monitorea el voltaje entrante del tomacorriente de pared y se conmuta automáticamente en consecuencia. Las fuentes de alimentación de conmutación automática aceptan voltajes de 100 a 240 VCA a 50 a 60 Hz. Estas fuentes de alimentación son populares en dispositivos móviles y son excelentes para viajes internacionales.

### Consejo técnico: encender una fuente de alimentación sin nada conectado podría dañarla

No enciendas una fuente de alimentación sin conectarla a la placa madre y posiblemente a un dispositivo como una unidad óptica o un disco duro. Una fuente de alimentación ATX generalmente requiere como mínimo una conexión a la placa madre.

### Factores de forma de la fuente de alimentación

Así como las placas madre vienen en diferentes formas y tamaños, también las fuentes de alimentación. Los factores de forma de las fuentes de alimentación actuales son ATX, ATX12V y micro-ATX. El factor de forma de la fuente de alimentación ATX fue el primero en permitir que se proporcionara una pequeña cantidad de voltaje a la placa madre para que tanto el hardware como el software pudieran usarse para "despertar" el dispositivo y/o reducir el voltaje para ahorrar energía. Esto se conocía como **interruptor suave** (soft switch).

El factor de forma de la fuente de alimentación micro-ATX es una versión más pequeña que una fuente de alimentación ATX de tamaño completo para caber en chasis más pequeños. Otros factores de forma incluyen LFX12V (perfil bajo), SFX12V (factor de forma pequeño), EPS12V (usado con placas madre de servidor), CFX12V (factor de forma compacto), SFX12V (factor de forma pequeño), TFX12V (factor de forma delgado), WTX12V (factor de forma de estación de trabajo para estaciones de trabajo de gama alta y servidores selectos) y FlexATX (para sistemas más pequeños).

Intel, AMD y los fabricantes de tarjetas de video certifican fuentes de alimentación específicas que funcionan con sus procesadores y tarjetas de video. Un fabricante de computadoras también puede tener un factor de forma de fuente de alimentación propietario que no es compatible con diferentes modelos de computadora ni con máquinas de otros proveedores. Las fuentes de alimentación de las laptops comúnmente son propietarias.

### Conectores de la fuente de alimentación

La Tabla 5.3 enumera los posibles conectores de una fuente de alimentación ATX, y la Figura 5.25 los muestra.

> Tabla 5.3 Conectores de la fuente de alimentación ATX

| Conector | Notas | Voltaje(s) |
|---|---|---|
| Conector de alimentación principal de 24 pines | Alimentación ATX principal a la placa madre | +3.3, +5, +12, −12 |
| Conector de alimentación SATA de 15 pines | Alimentación SATA interna | +3.3, +5, +12 |
| 12V de 8 pines | 12V para la CPU, usado con una fuente de alimentación ATX12V v1 | +12 |
| PCIe de 8 pines | Video PCIe; se conecta a un adaptador de video PCIe (Ten en cuenta que algunos conectores son de 6+2 pines, lo que significa que aceptan el cable de 6 u 8 pines). | +12 |
| PCIe de 6 pines | Video PCIe; se conecta a un adaptador de video PCIe | +12 |
| 6 pines | A veces etiquetado como AUX; se conecta a la placa madre si esta tiene un conector | +3.3, +5 |
| Molex de 4 pines | Se conecta a dispositivos periféricos como discos duros y unidades de CD/DVD | +5, +12 |
| Berg de 4 pines | Se conecta a dispositivos periféricos como una unidad de disquete | +5, +12 |
| 12V de 4 pines | A veces etiquetado como AUX o 12V; se conecta a la placa madre para la CPU | +12 |
| 3 pines | Se usa para monitorear la velocidad del ventilador | N/A |

> Figura 5.25 Conectores de la fuente de alimentación ATX

### Consejo técnico: la placa madre, el chasis y la fuente de alimentación deben ser compatibles en tamaño

El factor de forma de la placa madre y del chasis y el factor de forma de la fuente de alimentación deben caber en el chasis y deben funcionar juntos. Para un rendimiento óptimo, investiga qué conectores y factores de forma son compatibles con ambos componentes.

La Figura 5.26 ilustra los estándares del conector de placa madre ATX de 24 pines. Las fuentes de alimentación más antiguas tenían un conector de placa madre de 20 pines que podías enchufar directamente en el zócalo de placa madre de 24 pines (dejando los pines 11, 12, 23 y 24 vacíos), o podías comprar un **adaptador de placa madre de 20 a 24 pines**. Observa en la Figura 5.26 que el cable de alimentación es solo un conector, y el cable se inserta en el conector de una sola forma. Observa también que una señal de "power good" (etiquetada PWR_OK en la Figura 5.26) va a la placa madre. Cuando se enciende la computadora, parte de la POST es permitir que la fuente de alimentación ejecute una prueba en cada uno de los niveles de voltaje. Los niveles de voltaje deben ser correctos antes de que se prueben y permitan inicializar otros dispositivos. Si la alimentación está bien, se envía una señal de "power good" a la placa madre. Si la fuente de alimentación no envía la señal de "power good", un chip temporizador en la placa madre reinicia la CPU. Una vez que se envía una señal de "power good", la CPU comienza a ejecutar software desde el BIOS/UEFI. La Figura 5.26 también muestra la conexión +5VSB para proporcionar energía en espera para funciones como Wake on LAN o Wake on Ring (tratadas más adelante en este capítulo).

> Figura 5.26 Conectividad de placa madre ATX de 24 pines

La cantidad y el tipo de conectores disponibles en una fuente de alimentación dependen del fabricante de la fuente de alimentación. Si una tarjeta de video necesita un conector PCIe y hay dos conectores de alimentación Molex libres, se puede comprar un convertidor doble de Molex a PCIe. Si un dispositivo SATA necesita una conexión de alimentación y solo hay un cable Molex libre, hay disponible un convertidor de Molex a SATA. La Figura 5.27 muestra un convertidor doble de Molex a PCIe a la izquierda y un convertidor de Molex a SATA a la derecha.

> Figura 5.27 Convertidores dobles de Molex a PCIe y de Molex a SATA

Los conectores de la fuente de alimentación pueden conectarse a cualquier dispositivo; no hay un conector específico para el disco duro, la unidad óptica, etc. Si no hay suficientes conectores de la fuente de alimentación para la cantidad de dispositivos instalados en una computadora, se puede comprar un conector de alimentación en Y en una tienda de computadoras o electrónica.

### Propósitos de una fuente de alimentación

La energía de un tomacorriente de pared es CA de alto voltaje. El tipo de energía que necesitan las computadoras es CC de bajo voltaje. Todas las piezas de la computadora (los chips electrónicos de la placa madre y los adaptadores, la electrónica de las unidades y los motores del disco duro y la unidad óptica) necesitan energía de CC para funcionar. Las fuentes de alimentación en general vienen en dos tipos: lineales y conmutadas. Las computadoras usan fuentes de alimentación conmutadas. Las funciones principales de una fuente de alimentación incluyen las siguientes:

- Convertir CA a CC
- Proporcionar voltaje de CC a la placa madre, los adaptadores y los dispositivos periféricos
- Proporcionar enfriamiento y facilitar el flujo de aire a través del chasis

### Consejo técnico: comprobar el selector de voltaje de entrada

Algunas fuentes de alimentación y laptops tienen selectores de voltaje de entrada; otras tienen la capacidad de aceptar entrada de 100 a 240 volts para usar en varios países (doble voltaje). Asegúrate de que una fuente de alimentación acepte o esté configurada al voltaje de entrada adecuado.

Otro propósito de una fuente de alimentación es distribuir el voltaje de CC adecuado a cada componente. Varios cables con conectores salen de la fuente de alimentación. Con las placas madre ATX, solo hay un conector de 24 pines usado para conectar la energía a la placa madre. El conector de alimentación se inserta de una sola forma en el conector de la placa madre. La Figura 5.28 muestra un conector ATX que se inserta en una placa madre.

> Figura 5.28 Instalar un conector de alimentación ATX en una placa madre

Otro propósito de una fuente de alimentación es proporcionar enfriamiento a la computadora. El ventilador de la fuente de alimentación hace circular el aire por toda la computadora. La mayoría de los chasis de computadora tienen rejillas de ventilación en un lado, en ambos lados o en la parte trasera. La fuente de alimentación de estilo ATX sopla el aire hacia el interior del chasis en lugar de sacarlo por la parte trasera; con este método de enfriamiento de flujo inverso, el aire sopla sobre el procesador y la memoria para mantenerlos fríos. Este tipo de fuente de alimentación mantiene el interior de la computadora más limpio que los estilos más antiguos.

### Consejo técnico: no bloquear las rejillas de ventilación

Ya sea que una computadora sea un modelo de escritorio, un modelo de torre o un modelo de escritorio montado en un soporte en el piso, asegúrate de que nada bloquee las rejillas de ventilación del chasis de la computadora.

Debido a que los disipadores de calor generan mucho calor, es importante tener la cantidad adecuada de flujo de aire y en la dirección correcta. Se pueden instalar ventiladores adicionales para proporcionar enfriamiento adicional a una PC. La Figura 5.29 muestra ventiladores de enfriamiento adicionales instalados, así como luces LED que son populares en los chasis actuales.

> Figura 5.29 Ventilador auxiliar de chasis con iluminación LED

### Consejo técnico: flujo de aire y ventilación

El flujo de aire debe atravesar la computadora y pasar sobre la placa madre para proporcionar enfriamiento a los componentes de la placa madre.

Los chasis tienen diferentes cantidades y ubicaciones de puntos de montaje para el o los ventiladores del chasis. La Figura 5.30 muestra dos posibles sitios de instalación para un ventilador adicional.

### Consejo técnico: tener cuidado al instalar un ventilador auxiliar

Coloca un ventilador de modo que el flujo de aire de salida se mueva en la misma dirección que el flujo de aire generado por la fuente de alimentación. Si un ventilador auxiliar se instala dentro de un chasis en la ubicación incorrecta, el flujo de aire auxiliar podría oponerse al flujo de aire de la fuente de alimentación, reduciendo el efecto de enfriamiento.

> Figura 5.30 Colocación de ventiladores auxiliares

## Interfaz avanzada de configuración y energía (ACPI)

La **interfaz avanzada de configuración y energía (ACPI)** da al BIOS/UEFI y al sistema operativo control sobre la energía y los modos de operación de varios dispositivos. La ACPI tiene varios estados operativos, como se muestra en la Tabla 5.4.

> Tabla 5.4 Estados operativos de ACPI

| Estado global del sistema | Estado de suspensión | Descripción |
|---|---|---|
| G0 — En funcionamiento | S0 | La computadora es totalmente funcional. El software, como la función de autoguardado usada con productos de Microsoft, se puede optimizar para el rendimiento o para reducir el uso de la batería. |
| G1 — Durmiendo | (S1, S2, S3, S4) | Requiere menos energía que el estado G0 y tiene múltiples estados de suspensión: S1, S2, S3 y S4. |
| | S1 | La CPU sigue alimentada y los dispositivos no usados se apagan. La RAM se sigue refrescando. Los discos duros no están funcionando. |
| | S2 | La CPU no está alimentada. La RAM se sigue refrescando. El sistema se restaura instantáneamente ante la intervención del usuario. |
| | S3 | La salida de la fuente de alimentación se reduce. La RAM se sigue refrescando. Parte de la información de la RAM se restaura a la CPU y a la caché. |
| | S4 | El modo de suspensión de menor consumo, que es el que más tarda en activarse. La información de la RAM se guarda en memoria no volátil, como un disco duro o un medio flash. Algunos fabricantes lo llaman estado de hibernación. |
| G2 — Apagado suave (soft off) | S5 | El consumo de energía es casi cero. Requiere que el sistema operativo se reinicie. No se guarda información en ningún lugar. |
| G3 — Apagado mecánico | | También llamado apagado. Este es el único estado en el que la computadora se puede desmontar. Debes encender la computadora para usarla de nuevo. |

La ACPI permite que las aplicaciones trabajen con el sistema operativo para administrar la energía, como cuando una aplicación está configurada para guardar automáticamente un documento, pero podría no hacerlo hasta que el disco duro se esté usando para otra cosa, a fin de conservar energía en una laptop. En el entorno de Windows, el modo de suspensión, también conocido como modo de espera (suspend mode), usa uno de los estados de suspensión G1 de la ACPI para permitir que el dispositivo se despierte y continúe trabajando. El modo de hibernación usa el modo G1 S4 y es el que más tarda en devolver un dispositivo a un estado de funcionamiento.

### Consejo técnico: ¿qué opción de energía seleccionar, suspensión o hibernación?

La mayoría de las personas que quieren volver a acceder rápidamente a un dispositivo seleccionarían la opción de suspensión (standby). Sin embargo, el modo de hibernación ahorra más energía.

Dos funciones comunes del BIOS/UEFI y de los adaptadores que aprovechan la ACPI son Wake on LAN y Wake on Ring. La función **Wake on LAN** permite a un administrador de red controlar la energía de una estación de trabajo de forma remota y dirige a la computadora a salir del modo de suspensión. Las aplicaciones de software también pueden usar la función Wake on LAN para realizar actualizaciones, mejoras y tareas de mantenimiento. La función también se puede usar para encender las computadoras inmediatamente antes de que comience el día laboral. Wake on LAN se puede usar con cámaras web o de red para comenzar a grabar cuando se detecta movimiento o para encender una impresora de red para que se pueda usar cuando sea necesario.

**Wake on Ring** permite que una computadora salga del modo de suspensión cuando la línea telefónica tiene una llamada entrante. Le permite a la computadora recibir llamadas telefónicas, faxes y correos electrónicos cuando el usuario no está presente.

### Consejo técnico: ¿por qué dejar las computadoras encendidas en la oficina?

En Windows, cuando se apaga una computadora, se la pone en estado de apagado suave, o S5. Wake on LAN no es oficialmente compatible desde este estado, y por esta razón, los entornos corporativos solicitan que los usuarios dejen sus computadoras encendidas pero con la sesión cerrada en días específicos o todos los días.

### Reemplazar o actualizar una fuente de alimentación

Las fuentes de alimentación se clasifican en vatios. Las computadoras típicas de hoy tienen fuentes de alimentación con una clasificación de vataje que va de 250 a 500 vatios, aunque las computadoras potentes, como los servidores de red o los sistemas de juego de gama alta, pueden tener fuentes de alimentación clasificadas a 600 vatios o más. Los dispositivos internos y externos alimentados por un tipo particular de puerto, como USB, se ven afectados por la cantidad de amperios disponibles de la salida de energía de CC de +5 y +12V y la cantidad total de vataje disponible.

Cada dispositivo dentro de una computadora usa una cierta cantidad de energía, y la fuente de alimentación debe proporcionar suficiente energía para ejecutar todos los dispositivos. La energía que requiere cada dispositivo o adaptador generalmente se define en la documentación del dispositivo o adaptador o en el sitio web del fabricante. La computadora usa el vataje necesario, no la capacidad total de una fuente de alimentación.

### Consejo técnico: vigilar el vataje

Muchos fabricantes exageran el vataje. El vataje anunciado no es el vataje disponible a temperaturas más altas, como cuando está montado dentro de una computadora. Investiga un modelo antes de comprarlo.

Algunas fuentes de alimentación se anuncian como de doble o triple (o tri) riel. Una **fuente de alimentación de doble riel** tiene dos líneas de salida de +12V que se monitorean en busca de una condición de sobrecorriente. Una fuente de alimentación de triple riel simplemente tiene tres líneas de salida de +12V monitoreadas. Ten en cuenta que la mayoría de los fabricantes no tienen dos o más fuentes de 12V independientes; todas derivan de la misma fuente de 12V pero tienen líneas de salida independientes. La Figura 5.31 muestra cómo podrían usarse los rieles de +12V.

> Figura 5.31 Rieles de 12V

Algunas personas están interesadas en exactamente cuánta energía consume su sistema. Cada dispositivo en una computadora consume energía, y cada dispositivo puede usar uno o más niveles de voltaje diferentes (por ejemplo, +5V, −5V, +12V, −12V y +3.3V). Una fuente de alimentación tiene un amperaje máximo para cada nivel de voltaje (por ejemplo, 30 amperios a +5 volts y 41 amperios a +12V). Para determinar la potencia máxima que se usa, en vatios, multiplica los amperios por los volts. Si sumas todos los niveles de potencia máximos, la cantidad será mayor que la clasificación de la fuente de alimentación. Esto significa que no puedes usar la potencia máxima en cada nivel de voltaje; sin embargo, debido a que −5V y −12V no se usan muy a menudo, normalmente esto no es un problema.

### Cantidad de dispositivos/tipos de dispositivos que se van a alimentar

Para determinar la energía que se consume, debes investigar cada dispositivo para determinar cuánta corriente usa en un nivel de voltaje específico. Hay calculadoras de energía disponibles en internet para ayudar con esta tarea. Es importante tener una fuente de alimentación lo suficientemente potente para la cantidad de dispositivos y los tipos de dispositivos instalados en la computadora. La Tabla 5.5 enumera requisitos de energía de ejemplo de componentes de computadora.

> Tabla 5.5 Requisitos de energía de ejemplo de componentes de computadora

| Componente | Consumo de energía |
|---|---|
| Placa madre (sin procesador) | 5W a 150W |
| Procesador | 10W a 140W |
| Disco duro PATA IDE | 3W a 30W |
| Disco duro SATA | 2W a 15W |
| Unidad óptica | 10W a 30W |
| Adaptador sin video | 4W a 25W |
| Adaptador de video AGP | 20W a 50W |
| Tarjeta de video PCIe con un conector de alimentación | 50W a 150W |
| Tarjeta de video PCIe con dos conectores de alimentación | 100W a 300W |
| Ventilador adicional | 3W |
| Módulo de RAM | 15W |

### Elegir una fuente de alimentación

Al elegir una fuente de alimentación, lo primero que hay que considerar son el tamaño y el factor de forma, porque la fuente de alimentación tiene que caber en el chasis. Hay disponibles diferentes tamaños físicos de fuentes de alimentación, y algunas computadoras (especialmente servidores o equipo de red) tienen una **fuente de alimentación redundante** que se puede usar si una fuente de alimentación falla. Lo segundo que hay que considerar es el vataje: debes comprar una fuente de alimentación que tenga el mismo vataje o más que la fuente de alimentación original. Por último, no olvides asegurarte de que el interruptor de encendido/apagado de la nueva fuente de alimentación esté en una ubicación que se ajuste al chasis de la computadora.

### Consejo técnico: no todas las fuentes de alimentación son iguales

Un técnico necesita reemplazar una fuente de alimentación por una que proporcione una cantidad de energía igual o mayor. Busca en internet reseñas de fuentes de alimentación. Una regla general es que si dos fuentes de alimentación son iguales en vataje, la más pesada es mejor porque usa un transformador más grande, disipadores de calor más grandes y componentes de mayor calidad.

El **80 PLUS** es un sistema de clasificación de eficiencia de fuentes de alimentación que se ha incorporado a las especificaciones de ENERGY STAR. La eficiencia implica convertir más CA en CC. El sistema de clasificación consta de seis niveles de eficiencia, siendo 80 PLUS Titanium el más alto. Cada nivel debe proporcionar un nivel particular de eficiencia con una cantidad específica de carga (cantidad de componentes que se usan simultáneamente y que requieren energía).

Que una fuente de alimentación no esté certificada como 80 PLUS no significa que no sea una fuente de alimentación energéticamente eficiente, pero el nivel te da una idea de la diferencia entre fuentes de alimentación. Al elegir una fuente de alimentación, las cosas más importantes que hay que considerar son las siguientes:

- Tamaño y factor de forma
- Vataje
- Cantidad y tipo de conectores
- Eficiencia energética
- Cantidad de rieles de 12V monitoreados en busca de una condición de sobrecorriente

A algunas personas les gustan las funciones adicionales, como luces de colores dentro de la fuente de alimentación, el ventilador de la fuente de alimentación y/o los puertos. Una **fuente de alimentación modular** viene con cables desmontables (ver la Figura 5.32), de modo que los cables que no se usan simplemente no se sujetan a la fuente de alimentación para ayudar en la gestión de cables.

> Figura 5.32 Fuente de alimentación modular con puertos de cable desmontables

### Consejo técnico: valores de energía para monitores de bajo consumo

¡Mantén siempre el valor de tiempo de espera del protector de pantalla más corto que el valor de tiempo de espera del ahorro de energía, especialmente con monitores ecológicos (de bajo consumo)!

### Protección de energía

Las fuentes de alimentación tienen protección incorporada contra condiciones de energía adversas. Sin embargo, la mejor protección para una computadora es desenchufarla durante un corte de energía o una tormenta eléctrica. Los protectores contra sobretensiones y las **fuentes de alimentación ininterrumpida (UPS)** se usan comúnmente para protegerse contra condiciones de energía adversas. También se puede usar un acondicionador de línea. Cada dispositivo tiene un propósito específico y protege contra ciertas condiciones. Un técnico debe estar familiarizado con cada dispositivo para poder hacer recomendaciones a los clientes. La Figura 5.33 muestra un protector contra sobretensiones, y el Capítulo 19, «Procedimientos operativos», cubre estos dispositivos con más detalle.

> Figura 5.33 Protector contra sobretensiones Tripp Lite

### Síntomas de problemas de la fuente de alimentación

La fuente de alimentación a veces es una fuente de problemas inusuales. Los efectos de los problemas pueden ir desde los que el usuario no nota hasta los que apagan el sistema. La siguiente es una lista de síntomas de problemas de la fuente de alimentación:

- La luz de encendido está apagada y/o el dispositivo no se enciende (sin energía o pantalla negra).
- El ventilador de la fuente de alimentación no gira cuando se enciende la computadora.
- La computadora emite un pitido continuo. (Esto también podría ser una placa madre defectuosa o una tecla atascada en el teclado).
- Cuando se enciende la computadora, no emite ningún pitido. (Esto también podría ser una placa madre defectuosa).
- Cuando se enciende la computadora, emite pitidos cortos repetidos. (Esto también podría ser una placa madre defectuosa).
- Durante la POST, aparece un código de error de POST 02X o de paridad (donde X es cualquier número); una de las comprobaciones de la POST es una señal de "power good" de la fuente de alimentación, y un mensaje de error 021, 022, … indica que la fuente de alimentación no pasó la POST.
- La computadora se reinicia, se apaga sin previo aviso, tiene apagados intermitentes o se reinicia continuamente.
- El ventilador de la fuente de alimentación es ruidoso (emite un ruido fuerte o chirriante).
- La fuente de alimentación está demasiado caliente al tacto.
- La computadora emite olor a quemado, emite humo o se sobrecalienta.
- El ventilador de la fuente de alimentación gira, pero no llega energía a otros dispositivos.
- El monitor tiene una luz de encendido, pero no aparece nada en el monitor y no se ilumina ninguna luz de encendido de la PC.

### Comprobar los voltajes de la fuente de alimentación

Consulta la Figura 5.26 y observa cómo se emiten y suministran +3.3V, +5V, −5V, +12V y −12V a la placa madre (siendo +5V y +12V los voltajes más comunes suministrados a los dispositivos). La placa madre y los adaptadores usan +3.3V y +5V, pero rara vez se usa −5V. Las unidades mecánicas comúnmente usan +5V y +12V. El voltaje de +12V se usa para operar los motores de los dispositivos que se encuentran en las unidades, la CPU, los ventiladores de enfriamiento internos y la tarjeta de video. Los chips usan +5V y +3.3V, y +3.3V también se usa para la memoria, los adaptadores AGP/PCI/PCIe y algunos ventiladores de laptop. Los voltajes negativos rara vez se usan.

Un técnico debe comprobar ocasionalmente los voltajes en un sistema. Hay cuatro comprobaciones básicas para situaciones de la fuente de alimentación: (1) voltaje de CA del tomacorriente de pared, (2) voltajes de CC que van a la placa madre, (3) voltajes de CC que van a un dispositivo y (4) conexión a tierra o ausencia de voltaje con un probador de tomacorriente. Se puede usar un **probador de fuente de alimentación** para comprobar los niveles de energía de CC en los diferentes conectores de la fuente de alimentación. La Figura 5.34 muestra un probador de fuente de alimentación de PC. El tipo de conectores varía de un proveedor a otro, así que asegúrate de conseguir un probador que pueda manejar Molex, SATA y la alimentación principal del sistema como mínimo.

> Figura 5.34 Probador de fuente de alimentación de PC

### Resolver problemas de la fuente de alimentación

Cuando sospeches que una fuente de alimentación está causando un problema, ¡cambia la fuente de alimentación, haz feliz al cliente y sigue tu camino! Los problemas de energía no suelen ser difíciles de detectar o diagnosticar.

### Consejo técnico: no desmontar una fuente de alimentación

Las fuentes de alimentación normalmente no se desmontan. Los fabricantes a menudo las remachan para cerrarlas. Incluso cuando una fuente de alimentación se puede desmontar, no deberías abrirla a menos que tengas formación en electrónica.

No pases por alto los síntomas más obvios de la fuente de alimentación. Comienza revisando la luz de encendido de la computadora. Si está apagada, comprueba el ventilador de la fuente de alimentación colocando la palma de la mano en la parte trasera de la computadora. Si el ventilador está girando, significa que el tomacorriente de pared le está proporcionando energía a la computadora, y puedes asumir que el tomacorriente de pared está funcionando. Revisa la placa madre en busca de LED y consulta el manual para conocer su significado. Prueba el tomacorriente con otro dispositivo. Asegúrate de que el cable de alimentación esté insertado por completo en el tomacorriente de pared y en la computadora. Si sospechas que el tomacorriente de pared está defectuoso, usa un **probador de circuito de CA** para verificar que el tomacorriente de pared esté cableado correctamente.

Las siguientes preguntas de diagnóstico pueden ayudarte a determinar la ubicación de un problema de energía:

- ¿La fuente de alimentación funcionaba antes? Si no, revisa el interruptor selector de voltaje de entrada en la fuente de alimentación y verifica que esté en la configuración correcta.
- ¿El ventilador de la fuente de alimentación está girando? Si es así, revisa los voltajes que van a la placa madre. Si son buenos, quizás solo el ventilador de la fuente de alimentación esté defectuoso. Si el ventilador de la fuente de alimentación no está girando, revisa el tomacorriente de pared en busca de voltajes de CA correctos.
- ¿Se usa una regleta contra sobretensiones? Si es así, verifica si la regleta contra sobretensiones está encendida y luego prueba un tomacorriente diferente en la regleta o reemplaza la regleta.
- ¿El cable de alimentación de la computadora está bien? Verifica que el cable de alimentación se enchufe firmemente en el tomacorriente y en la parte trasera de la computadora. Cambia el cable de alimentación para verificar que funcione.
- ¿El botón de encendido del panel frontal está atascado?
- ¿Los voltajes que van a la placa madre están en los niveles adecuados? Si son bajos, algo podría estar sobrecargando la fuente de alimentación. Desconecta el cable de alimentación de un dispositivo y vuelve a comprobar los voltajes. Vuelve a conectar el cable de alimentación al dispositivo. Retira el cable de alimentación de otro dispositivo y vuelve a comprobar los voltajes de la placa madre. Continúa haciendo esto hasta que se haya desconectado el cable de alimentación de cada dispositivo y se hayan comprobado los voltajes de la placa madre. Un solo dispositivo puede cortocircuitar la fuente de alimentación y hacer que el sistema funcione mal. Reemplaza cualquier dispositivo que reduzca el voltaje de salida de la fuente de alimentación y consuma demasiada corriente. Si ninguno de los dispositivos es la causa del problema, reemplaza la fuente de alimentación. Si reemplazar la fuente de alimentación no resuelve el problema, reemplaza la placa madre.

Si una computadora no arranca correctamente pero sí arranca cuando presionas + + , es probable que la señal de "power good" sea el problema. Algunas placas madre son más sensibles a la señal de "power good" que otras. Por ejemplo, digamos que se reemplazó una placa madre y el sistema no arranca. A primera vista, esto podría parecer una placa de reemplazo defectuosa, pero el problema podría ser causado por una fuente de alimentación que no emite una señal de "power good" consistente, así que intenta reemplazar la fuente de alimentación.

### Consejo técnico: comprobar la señal de "power good"

Consulta la documentación de la fuente de alimentación para ver si la fuente de alimentación emite una señal de "power good", a veces llamada señal de "power OK", en lugar del +5V normal. Enciende la computadora. Comprueba la señal de "power good" en el conector de alimentación principal de la placa madre (sujeto a la fuente de alimentación). Haz esto antes de reemplazar la placa madre. Una fuente de alimentación cuya señal de "power good" esté por debajo de +3V debe reemplazarse.

A veces, cuando una computadora sale del modo de suspensión, no todos los dispositivos responden, y hay que presionar el botón de encendido o de reinicio de la computadora para reiniciarla. Las siguientes situaciones pueden causar que esto ocurra:

- Un protector de pantalla entra en conflicto con la ACPI. Configura el protector de pantalla en Ninguno para ver si está causando el problema.
- Uno o más adaptadores/dispositivos no son compatibles con la ACPI.
- Un adaptador/dispositivo tiene un controlador desactualizado.
- El BIOS/UEFI del sistema o el BIOS de un adaptador instalado necesita actualizarse.

Para ver si el protector de pantalla causa un problema, usa Configuración de Personalización > vínculo Configuración del protector de pantalla y configura la opción de protector de pantalla en Ninguno. Identificar un adaptador, dispositivo o controlador problemático requiere investigar en internet. Revisa cada adaptador, dispositivo y controlador individualmente. Usa el Panel de control de Opciones de energía para cambiar el plan de energía. Para cada dispositivo, busca una pestaña Administración de energía en el cuadro de diálogo Propiedades y haz cambios si es necesario.

## Habilidades blandas: habilidades de comunicación escrita

Cuando los técnicos están en la escuela, rara vez piensan que las habilidades que deberían aprender impliquen la escritura. Sin embargo, en el lugar de trabajo, los técnicos usan habilidades de comunicación escrita cuando documentan problemas y usan el correo electrónico (ver la Figura 5.35). Los comités asesores de todo el país dicen que, además de tener conocimientos técnicos, es importante que los técnicos puedan comunicarse eficazmente tanto por escrito como oralmente, y que se sientan cómodos trabajando en un entorno de equipo. Además, los técnicos deben poseer habilidades de pensamiento crítico, es decir, ser capaces de resolver un problema sin que se les haya enseñado sobre ese problema específico.

> Figura 5.35 Los técnicos deben proporcionar con frecuencia comunicación escrita

Independientemente del tamaño de una empresa, normalmente se requiere documentación. La documentación podría ser solo la cantidad de horas dedicadas a un trabajo y una descripción básica de lo que se hizo, pero la mayoría de las empresas requieren un poco más. La documentación debe escribirse de manera que otros puedan leerla y comprenderla. Ten en cuenta que si otro técnico debe resolver otro problema del mismo cliente, una buena documentación ahorra tiempo y dinero. La siguiente es una lista de quejas de los gerentes que contratan técnicos:

- Evita hacer la documentación de manera oportuna.
- No proporciona información adecuada o precisa sobre lo que se realizó o se intentó.
- Tiene habilidades deficientes de ortografía, gramática, uso de mayúsculas y puntuación.
- Escribe en oraciones cortas y entrecortadas, usando jerga técnica.
- No proporciona actualizaciones sobre el estado de un problema.

Puedes usar esta lista para saber dónde mejorar tus habilidades y evitar cometer los mismos errores.

El correo electrónico es un medio de comunicación común para los técnicos. Sin embargo, la mayoría de los técnicos no se toman el tiempo de comunicarse eficazmente por correo electrónico. La siguiente es una lista de pautas para una comunicación eficaz por correo electrónico:

- No uses el correo electrónico cuando una reunión o una llamada telefónica sea más apropiada.
- Incluye una breve descripción del tema del correo electrónico en la línea de asunto.
- No escribas ni respondas un correo electrónico cuando estés enojado.
- Envía el correo electrónico solo a las personas apropiadas; no copies a otras innecesariamente.
- Cíñete al punto; no te desvíes.
- Usa un corrector de ortografía y gramática; si no se incluye uno en el cliente de correo electrónico, escribe el correo electrónico en una aplicación de procesamiento de textos, revísalo y luego pega el documento en el cuerpo del correo electrónico.
- Usa gramática, puntuación y uso de mayúsculas adecuados; no escribas todo en mayúsculas ni todo en minúsculas.
- Sonríe cuando escribes. Tu buena actitud se reflejará en tu escritura.
- Concéntrate en la tarea que tienes entre manos. Lee tu nota en voz alta si es crítica.
- Escribe cada correo electrónico como si estuvieras poniendo el mensaje en una valla publicitaria (ver la Figura 5.36); nunca sabes cómo podría usarse el contenido o quién podría verlo.

La queja número uno sobre el personal de soporte técnico no es su falta de habilidades técnicas, sino su falta de habilidades de comunicación. Dedica tanto tiempo de tu educación a practicar tus habilidades de comunicación como lo haces a tus habilidades técnicas.

> Figura 5.36 Piensa en lo que escribes en las comunicaciones escritas; podría hacerse público

## Resumen del capítulo

- Usar una pulsera de muñeca o mantener contacto con metal sin pintar mantiene a ti y a un dispositivo informático al mismo potencial eléctrico, de manera que no induzcas corriente en ninguna pieza ni la debilites/dañes.
- La EMI y la RFI causan problemas. Mueve una computadora o un dispositivo problemático y reemplaza todas las cubiertas de ranura/aperturas.
- Al retirar piezas, ten las herramientas correctas, iluminación y artículos antiestáticos, así como un espacio de trabajo amplio. Toma notas. No uses herramientas magnetizadas. Evita sacudir los discos duros.
- Ten cuidado al instalar un escudo de E/S y sé consciente de los separadores al tratar con la placa madre.
- Los procedimientos de mantenimiento preventivo prolongan la vida de una computadora. Aspira antes de rociar aire comprimido.
- Una MSDS/SDS describe los procedimientos de eliminación y almacenamiento y contiene información sobre toxicidad y preocupaciones de salud. Las ciudades/estados tienen reglas específicas de eliminación para sustancias químicas, baterías, electrónica, etc. Conoce siempre las reglas de eliminación del área donde trabajas.
- La energía de CA entra a una fuente de alimentación o al ladrillo de alimentación de un dispositivo móvil. Se proporciona energía de CC a todas las piezas internas de un dispositivo informático. Se pueden hacer comprobaciones de voltaje de CA y CC, y solo con la energía de CC importa la polaridad. Usa la configuración más alta posible del medidor con niveles de voltaje desconocidos. La potencia se mide en vatios.
- Las comprobaciones de continuidad se hacen en el cableado, y un cable en buen estado muestra cerca de 0 ohmios.
- Una fuente de alimentación convierte CA a CC, distribuye CC por toda la unidad y proporciona enfriamiento. La fuente de alimentación debe tener el factor de forma correcto y ser capaz de suministrar la cantidad correcta de vataje para un nivel de voltaje particular, como +5V o +12V. Comúnmente hay disponibles múltiples "rieles" para +12V porque la CPU comúnmente necesita su propia conexión. Los números y tipos de conectores varían, pero se pueden comprar convertidores.
- Usa la ACPI para controlar las opciones de energía a través del BIOS/UEFI y el sistema operativo. Wake on LAN y Wake on Ring son funciones de energía que permiten que un dispositivo se encienda desde una condición de energía reducida para un propósito específico.
- Los probadores de circuito de CA, los multímetros y los probadores de fuente de alimentación son herramientas usadas con problemas de energía.
- En todas las comunicaciones y la documentación escrita, sé profesional y eficaz. Usa uso de mayúsculas, gramática, puntuación y ortografía adecuados.

## Consejos para el examen de certificación A+

- Revisa el resumen del capítulo. No olvides que otros capítulos también tienen consejos de mantenimiento preventivo, incluidos los capítulos sobre dispositivos de almacenamiento, dispositivos multimedia, impresoras y otros periféricos.
- Recuerda siempre apagar una computadora, retirar el cable de alimentación/ladrillo de alimentación/batería y permitir que una impresora láser se enfríe antes de realizar mantenimiento.
- Familiarízate con el manejo y almacenamiento adecuados de los componentes, incluido el uso de técnicas de autoconexión a tierra, bolsas antiestáticas, correas ESD y tapetes ESD.
- Conoce el propósito de una MSDS.
- Ten en cuenta que, tanto con los problemas de seguridad como al tratar con sustancias químicas y componentes que podrían tener un impacto ambiental potencial, el personal de TI debe cumplir con las regulaciones del gobierno local.
- Conoce el propósito de una correa ESD antiestática, tapetes ESD, bolsas antiestáticas y técnicas de autoconexión a tierra. No uses una correa ESD antiestática cuando trabajes dentro de un monitor CRT antiguo o una fuente de alimentación.
- Usa gafas de seguridad y una mascarilla de filtración de aire para protegerte de las partículas suspendidas en el aire.
- Sé consciente de los riesgos de temperatura, los efectos de la humedad en el equipo electrónico y cuándo se necesita ventilación.
- Sé capaz de identificar y explicar los cables básicos de disco duro SCSI, SATA, eSATA e IDE (incluida la alimentación, como se analiza en el Capítulo 7, «Dispositivos de almacenamiento»).
- Ten en cuenta que las fuentes de alimentación más antiguas tienen un cable de placa madre de 20 pines que se puede usar en un conector de placa madre de 24 pines, o se puede comprar un adaptador de placa madre de 20 a 24 pines.
- Identifica los tipos de conector comunes, como un conector Molex.
- Ten en cuenta que la fuente de alimentación emite 3.3V, 5V y 12V y que la electrónica comúnmente usa 5V y los motores usan 12V. Si una computadora se va a usar internacionalmente, asegúrate de que admita una fuente de alimentación de conmutación automática que acepte 110V o 220 VCA como voltaje de entrada.
- Comprende los requisitos de energía de los componentes de la computadora y que la fuente de alimentación debe ser lo suficientemente potente para alimentar la cantidad de dispositivos y los tipos de dispositivos instalados en la computadora.
- Familiarízate con los síntomas comunes de problemas de energía, incluido el ventilador que gira pero no se proporciona energía a otros dispositivos, la falta de energía, el ventilador ruidoso o inoperante, y la computadora que se reinicia o se apaga sin previo aviso.
- Familiarízate con las conexiones de la placa madre a los paneles superior y frontal (USB, audio, botón de encendido, luz de encendido, luces de actividad de la unidad y botón de reinicio).
- Las siguientes habilidades de comunicación y profesionalismo son parte del examen 220-1102: usar lenguaje adecuado y evitar jerga, acrónimos y argot cuando corresponda; y proporcionar documentación adecuada sobre los servicios prestados.

## Términos clave

- 12V
- 3.3V
- 5V
- Voltaje de entrada de 110V vs. 220V — *110V vs. 220V input voltage*
- Adaptador de placa madre de 20 a 24 pines — *20-pin to 24-pin motherboard adapter*
- Conector de placa madre de 24 pines — *24-pin motherboard connector*
- 12V de 4 pines — *4-pin 12V*
- PCIe de 6 pines — *6-pin PCIe*
- PCIe de 8 pines — *8-pin PCIe*
- CA — *AC*
- Probador de circuito de CA — *AC circuit tester*
- ACPI
- Mascarilla de filtración de aire — *air filtration mask*
- Amperio — *amp*
- Bolsa antiestática — *antistatic bag*
- Pulsera antiestática — *antistatic wrist strap*
- Pantalla negra — *black screen*
- Olor a quemado — *burning smell*
- Aire comprimido — *compressed air*
- Reinicio de la computadora — *computer reboot*
- Continuidad — *continuity*
- CC — *DC*
- Fuente de alimentación de doble riel — *dual-rail power supply*
- EMI
- Conexión a tierra del equipo — *equipment grounding*
- ESD
- Tapete ESD — *ESD mat*
- Correa ESD — *ESD strap*
- Conector del panel frontal — *front panel connector*
- Ruido chirriante — *grinding noise*
- Escudo de E/S — *I/O shield*
- Cable IDE — *IDE cable*
- Apagado intermitente — *intermittent shutdown*
- Kit de mantenimiento — *maintenance kit*
- Fuente de alimentación modular — *modular power supply*
- Molex
- MSDS
- Sin energía — *no power*
- Ohmio — *ohm*
- Sobrecalentamiento — *overheating*
- Potencia — *power*
- Probador de fuente de alimentación — *power supply tester*
- Mantenimiento preventivo — *preventive maintenance*
- Fuente de alimentación redundante — *redundant power supply*
- Resistencia — *resistance*
- RFI
- Gafas de seguridad — *safety goggles*
- Conector SATA — *SATA connector*
- Autoconexión a tierra — *self-grounding*
- SDS
- Humo — *smoke*
- Separador — *standoff*
- Aspiradora para tóner — *toner vacuum*
- Voltio — *volt*
- Voltaje — *voltage*
- Wake on LAN
- Wake on Ring
- Vatio — *watt*
- Clasificación de vataje — *wattage rating*
- Comunicación escrita — *written communication*

## Preguntas de repaso

1. ¿Qué ocurriría si retiras accidentalmente la batería de una placa madre?
2. Enumera tres tareas que se realizan comúnmente durante el mantenimiento preventivo.
3. Las computadoras usadas en un almacén de supermercado para el control de inventario tienen una tasa de falla de piezas más alta que las demás computadoras de la empresa. ¿Cuál de las siguientes opciones es más probable que ayude en esta situación?
   a. una pulsera antiestática
   b. un plan de mantenimiento preventivo
   c. almohadillas antiestáticas
   d. fuentes de alimentación de alto vataje

4. ¿Cuál de las siguientes opciones puede prolongar la vida de una computadora y ahorrar energía? (Elige todas las que correspondan.)
   a. un plan de mantenimiento preventivo
   b. tapetes y almohadillas antiestáticas
   c. fuente de alimentación actualizada
   d. un plan de energía
   e. baterías de reemplazo de Li-ion
   f. ventiladores de chasis adicionales

5. ¿Qué componente de energía tiene un conector de 24 pines?
   a. conector principal de la placa madre
   b. ventilador de la fuente de alimentación
   c. ventilador del chasis
   d. alimentación AUX para la CPU

6. Una unidad óptica queda disponible aleatoriamente y, después de reemplazar la unidad, el técnico ahora sospecha que la unidad podría no estar recibiendo 5 volts de manera constante. ¿Qué podría ayudar en esta situación?
   a. una UPS
   b. un protector contra sobretensiones
   c. toallitas antiestáticas
   d. un plan de mantenimiento preventivo
   e. un probador de fuente de alimentación

7. Al desmontar una computadora, ¿qué herramienta te ayudará a retirar el módulo de memoria?
   a. destornillador magnético
   b. alicates de punta larga
   c. destornillador Phillips n.º 1 o n.º 2
   d. pulsera antiestática

8. Un usuario tuvo un problema de placa madre la semana pasada y un técnico lo solucionó. Ahora la misma computadora tiene un problema diferente. El usuario informa que los puertos USB del frente ya no funcionan. ¿Qué es lo primero que deberías revisar?
   a. fuente de alimentación
   b. conexión de alimentación al panel frontal
   c. conexiones de la placa madre al panel frontal
   d. salida de voltaje de la fuente de alimentación a los conectores USB

9. ¿Cuál de los siguientes artículos estaría especializado para usar con una impresora láser?
   [ regleta contra sobretensiones | aspiradora | probador de fuente de alimentación | pulsera antiestática ]

10. ¿Cuáles dos de los siguientes elementos probablemente causarían un ruido fuerte en una computadora de escritorio? (Elige dos.)
    [ placa madre | unidad USB | fuente de alimentación | ventilador del chasis | memoria | adaptador PCIe ]

11. Una computadora no enciende. ¿Cuál de los siguientes se usaría para revisar el tomacorriente de pared?
    [ probador de fuente de alimentación | UPS | multímetro | POST ]

12. Una computadora no enciende. Después de revisar el tomacorriente de pared y cambiar el cable de alimentación, ¿qué usaría el técnico a continuación?
    a. resistencia
    b. probador de fuente de alimentación
    c. pulsera antiestática
    d. destornillador magnético
    e. destornillador no magnético

13. ¿Cuál de los siguientes se ve afectado por la clasificación de vataje de la fuente de alimentación?
    a. cantidad de adaptadores y dispositivos de almacenamiento internos
    b. cantidad de conectores de la fuente de alimentación
    c. velocidad del procesador
    d. tipo de procesador
    e. tipo de conectores de la fuente de alimentación

14. ¿Cuál de los siguientes ayudaría con el calor de la computadora?
    a. aumentar el vataje de la fuente de alimentación
    b. actualizar a un factor de forma de fuente de alimentación más grande
    c. desconectar los conectores de alimentación no usados
    d. instalar ventiladores de chasis

15. [ V | F ] El desmontaje de la fuente de alimentación es un requisito común de un técnico de PC.

16. Considera el siguiente correo electrónico.
    De: Cheryl a. Schmidt
    Para: Personal docente de Tecnología de Ingeniería de Redes
    Asunto: [Ninguno]
    Tenemos poco tiempo para hacer el PMS en las PC y el equipo de N/W. ¿Qué software quieres?

    Reformula este correo electrónico para ilustrar buenas habilidades de comunicación escrita.
    Las respuestas variarán, pero la siguiente es una respuesta de ejemplo:
    De: Cheryl A. Schmidt
    Para: Personal docente de Tecnología de Ingeniería de Redes
    Asunto: Software para el período de primavera
    Durante las vacaciones, realizaremos actualizaciones y mantenimiento en el equipo del departamento. También podríamos instalar cualquier actualización de software o nuevo software que necesitarás para el período de primavera. Por favor, reúnete conmigo o envíame un correo electrónico con tus requisitos. Recuerda que cualquier software debe comprarse y debe tener la licencia correspondiente antes de que pueda instalarlo. Por favor, contáctame si tienes alguna pregunta.
    Atentamente,
    Cheryl Schmidt, Técnica de Computadoras

17. Enumera tres recomendaciones para una buena comunicación técnica escrita.
18. Una computadora está haciendo cosas extrañas, como apagarse inesperadamente y colgarse. Sospechas de un problema de energía. Compruebas la señal de "power good" (power OK) en el conector principal de la placa madre de la fuente de alimentación. La lectura de voltaje muestra que tienes energía (+2.5 volts). ¿Qué vas a hacer a continuación?
    a. Revisar el voltaje que sale de un conector Molex o SATA.
    b. Revisar el voltaje del tomacorriente de pared.
    c. Reemplazar la fuente de alimentación.
    d. Revisar la resistencia del cable de la fuente de alimentación.

19. ¿Cuál es el propósito del escudo de E/S?
    a. Evita que el polvo y la suciedad entren a través de los puertos frontales de la computadora.
    b. Proporciona conexión a tierra para los puertos de la placa madre.
    c. Evita que el polvo y la suciedad entren en la fuente de alimentación.
    d. Protege a un técnico de las descargas.

20. ¿Qué dos artículos ayudarían a un técnico a mantener la seguridad personal mientras trabaja en PC e impresoras en un almacén extremadamente polvoriento? (Elige dos.)
    [ aspiradora | aspiradora para tóner | gafas de seguridad | pulsera antiestática | mascarilla de filtración de aire ]

## Ejercicios

**Ejercicio 5.1 Identificar los conectores de la fuente de alimentación**

Objetivo:
 Poder identificar los propósitos de los conectores comunes de la fuente de alimentación

Procedimiento:
 Identifica los conectores de la fuente de alimentación en la Figura 5.37.

> Figura 5.37 Identificación de conectores de alimentación

____ 1. Molex para unidad óptica antigua
____ 2. SATA para disco duro
____ 3. Video PCIe
____ 4. Placa madre principal
____ 5. CPU

**Ejercicio 5.2 Reconocer piezas de repuesto de una computadora**

Objetivo:
 Poder reconocer piezas de una computadora

Procedimiento:
 Usa la siguiente información para responder las preguntas.

Las siguientes piezas fueron pedidas por alguien que está construyendo su propia computadora:

a. Intel Core i7 4.4 GHz
b. ASUS Rampage V Extreme X99 (no incluye cabeceras USB 3.1)
c. Triage 8 GB
d. Micro-ATX con dos bahías internas de 3.5" y dos bahías externas de 5.25"
e. EVA 450W

1. ¿Qué pieza designa la letra a?
   [ memoria | disco duro | unidad óptica | CPU ]
2. ¿Qué pieza designa la letra b?
   [ placa madre | procesador | memoria | disco duro ]
3. ¿Qué pieza designa la letra c?
   [ placa madre | unidad óptica | RAM | disco duro SATA | SSD ]
4. ¿Qué pieza designa la letra d?
   [ RAM | chasis | todos los dispositivos de almacenamiento | fuente de alimentación ]
5. ¿Qué pieza designa la letra e?
   [ chasis | SSD | unidad óptica | fuente de alimentación ]

**Ejercicio 5.3 Describir las piezas de la computadora**

Objetivo:
 Poder reconocer las piezas de la computadora según una descripción

Procedimiento:
 Relaciona la descripción con la pieza de la computadora afectada durante el desmontaje.

____ 1. Conector de 24 pines
   a. Cable de la fuente de alimentación a la placa madre
____ 2. Cable plano de 40 pines
   b. Cable del panel frontal a la placa madre
____ 3. Bolsa antiestática
   c. Cable del disco duro a la placa madre
____ 4. Correa ESD
   d. Placa madre a dispositivo IDE PATA
____ 5. Conexión a tierra
   e. Se sujeta a la muñeca y a la computadora
____ 6. Disco duro
   f. Guarda un adaptador cuando no está en uso
____ 7. LED del HDD
   g. Ayuda con la EMI
____ 8. SATA 3
   h. Mantener contacto con la computadora
____ 9. Cubierta de ranura
   i. Sujeta la placa madre al chasis
____ 10. Separadores
   j. Podría necesitar rieles guía

## Actividades

**Descubrimiento en internet**

Objetivo:
 Obtener información específica en internet sobre una computadora o sus partes asociadas

Partes:
 Computadora con acceso a internet

Procedimiento:
 Completa el siguiente procedimiento y responde las siguientes preguntas.

1. Ubica un sitio de internet que proporcione consejos para hacer mantenimiento preventivo de computadoras.
   Escribe dos de los mejores consejos y la URL donde encontraste la información.
2. Ubica un sitio de internet donde puedas comprar un kit de herramientas de computadora que incluya una pulsera antiestática.
   Enlista la URL donde encontraste el kit y al menos tres tamaños de destornilladores o puntas provistos.
3. Ubica un probador de fuente de alimentación que incluya un conector SATA.
   Enlista el fabricante y el modelo.
4. Encuentra un sitio web sobre buenas normas de etiqueta en la red (netiquette).
   Da tres recomendaciones y el nombre del sitio web (no la URL).
5. Acabas de empezar a trabajar en un lugar que usa la computadora todo-en-uno HP Elite 800 G2 de 23 pulgadas sin pantalla táctil.
   Te han enviado a hacer comprobaciones de energía en la fuente de alimentación de una de estas unidades. ¿Cómo quitas la cubierta? Explícalo en detalle, usando oraciones completas.
   ¿Qué recomendación da HP para limpiar las manchas difíciles que se pueden encontrar en los chasis de las computadoras en el taller de mantenimiento?
   Según la documentación, ¿qué es diferente al retirar un procesador AMD que al retirar un procesador Intel?

**Habilidades blandas**

Objetivo:
 Mejorar y afinar la capacidad de un futuro técnico para escuchar, comunicarse tanto de forma escrita como oral, y apoyar de manera profesional a las personas que usan computadoras

Actividades:

1. Prepara una propuesta comercial para una fuente de alimentación de reemplazo para una computadora específica. Indica la computadora y presenta tu propuesta a la clase.
2. Escribe un informe informal sobre las habilidades aprendidas al desarmar y volver a armar una computadora. Comparte tus mejores prácticas con un grupo pequeño.
3. Trabajen en equipos para decidir la mejor manera de informar a un cliente sobre las diferencias entre una fuente de alimentación ATX y una SFX. Presenten su descripción a la clase como si estuvieran hablando con el cliente. Podrían considerar mostrar placas madre y chasis para ayudar a ilustrar su punto. Cada miembro del equipo debe contribuir. Cada compañero de clase vota por la mejor explicación del equipo.

**Habilidades de pensamiento crítico**

Objetivo:
 Analizar y evaluar información, así como aplicar la información aprendida a situaciones nuevas o diferentes

Actividades:

1. Usa internet para encontrar la descripción de una computadora en particular que enumere cada dispositivo que está instalado y el tipo de placa madre, los puertos integrados, etc. Luego ubica una calculadora de fuente de alimentación. Encuentra una fuente de alimentación de reemplazo, según los cálculos realizados. Escribe los detalles de lo que buscaste en la fuente de alimentación de reemplazo: la fuente de alimentación, el proveedor, la cantidad y el tipo de conectores y el costo.
2. Para una de las computadoras del aula, ubica la documentación sobre cómo desmontarla. Revisa la documentación y encuentra al menos tres buenos consejos que quizás no se te hayan ocurrido de inmediato si estuvieras desmontando la computadora. Luego encuentra al menos tres consejos de seguridad. Coloca toda esta información en un esquema. Una alternativa es ser creativo y presentar los consejos gráficamente en una página o diapositiva de presentación.
