# Capítulo 4. Introducción a la configuración

> Traducción al español del Capítulo 4 («Introduction to Configuration») de *Complete A+ Guide to IT Hardware and Software: CompTIA A+ Exams 220-1101 & 220-1102* (Cheryl A. Schmidt, Christopher Lee) — material de estudio de uso personal.
>
> Nota: las figuras del libro son imágenes y no se incluyen aquí; se conserva su leyenda traducida como referencia. Las tablas se transcriben como tablas de Markdown.

En este capítulo aprenderás:

- La importancia de BIOS y UEFI
- Cómo reemplazar la batería de la placa madre
- Qué son los recursos del sistema y cómo verlos/cambiarlos
- Pasos básicos para instalar, configurar y verificar dispositivos periféricos comunes y tarjetas USB, eSATA y de red
- Cómo solucionar problemas de configuración y de dispositivos

**Objetivos del examen CompTIA:**

- 1101-3.1 Explicar los tipos básicos de cable y sus conectores, características y propósitos.
- 1101-3.4 Dado un escenario, instalar y configurar placas madre, unidades centrales de procesamiento (CPU) y tarjetas adicionales.
- 1101-5.2 Dado un escenario, diagnosticar problemas relacionados con placas madre, RAM, CPU y energía.

## Descripción general de la configuración

Instalar y configurar la placa madre, el procesador, la RAM u otros dispositivos puede implicar el uso del programa de Setup del BIOS/UEFI del sistema o del sistema operativo. También te permite establecer opciones de rendimiento.

## Descripción general del BIOS

El **sistema básico de entrada/salida (BIOS)** es un componente importante de la placa madre que comúnmente está soldado a ella, como se muestra en la Figura 4.1. El BIOS también se conoce como **Unified Extensible Firmware Interface (UEFI)** y, a veces, simplemente como EFI, BIOS/UEFI o UEFI/BIOS. El BIOS tiene las siguientes funciones:

- Contiene y ejecuta la **autoprueba de encendido (POST)**: un programa que identifica, prueba e inicializa los componentes básicos de hardware.
- Contiene una rutina básica llamada **programa de arranque** (*bootstrap*) que localiza un sistema operativo y lo inicia, permitiendo que el sistema operativo tome el control del sistema.
- Contiene **Setup**, que es un programa que permite ver y gestionar ajustes relacionados con la pantalla, la fecha/hora, el procesador, la memoria y las unidades. Otros nombres usados para Setup incluyen BIOS Setup, System Setup y CMOS Setup.
- Opcionalmente, cede el control al BIOS integrado de un adaptador (tarjeta) para que la tarjeta pueda inicializarse durante el proceso de arranque de la computadora.

> Figura 4.1 BIOS de la placa madre

POST realiza pruebas básicas de componentes de hardware individuales, como la placa madre, los módulos de RAM, el teclado, la unidad óptica y el disco duro. POST se ejecuta cuando se realiza un **arranque en frío** (encender la computadora). Una indicación de que POST se está ejecutando es que las luces indicadoras del teclado parpadean momentáneamente y luego se apagan.

### Consejo técnico: acelerar el tiempo de arranque

El BIOS puede configurarse para limitar la cantidad de dispositivos que POST comprueba, reduciendo así el tiempo de arranque.

En contraste, reiniciar la computadora se conoce como **arranque en caliente**. En Windows, haz clic con el botón derecho en el botón Inicio > Apagar o cerrar sesión > Reiniciar. El arranque en caliente hace que los cambios realizados surtan efecto sin someter a la computadora a la misma tensión que un arranque en frío. Un arranque en caliente no ejecuta POST.

El programa Setup se guarda en el BIOS y, a través de él, puedes ver y posiblemente configurar o deshabilitar cosas como la RAM, el tipo y la cantidad de unidades instaladas, dónde busca la computadora sus archivos de arranque, la fecha y hora actuales, etc.

Hay dos formas principales de configurar un sistema o un adaptador: mediante el programa Setup guardado en el BIOS del sistema y mediante el sistema operativo. Examinemos primero el uso del programa Setup.

### Consejo técnico: ¿qué hacer si no puedes entrar a Setup?

Si no aparece nada en el monitor y la pantalla tiene energía y tienes una buena conexión al puerto de video, revisa la placa madre por si hay LED (CPU, RAM, pantalla/VGA, arranque, etc.) e investiga qué significa si el LED permanece encendido. Comprueba la instalación de la CPU, el ventilador de la CPU y la RAM.

## El programa Setup

Las computadoras tienen software de Setup integrado en el chip del BIOS del sistema en la placa madre, al que puedes acceder con teclas específicas (como Esc, Insert, Del, F1, F2, F10, o la combinación de teclas Ctrl + Alt + alguna otra tecla), determinadas por el fabricante del BIOS. Durante el proceso de arranque, la mayoría de las computadoras muestran un mensaje que indica qué tecla(s) iniciarán el programa Setup. El mensaje mostrado suele estar en una de las cuatro esquinas de la pantalla (ver la Figura 4.2).

> Figura 4.2 Teclas para entrar a Setup

### Consejo técnico: acceder al BIOS Setup desde Windows 10/11

Para acceder al BIOS Setup en Windows, ve a Configuración > Actualización y seguridad (10) o Sistema (11) > Recuperación > Reiniciar ahora.

## Flash BIOS

**Flash BIOS** te permite actualizar (o degradar) el BIOS sin instalar un nuevo chip o chips. Entre los fabricantes comunes de BIOS/UEFI de computadoras se incluyen AMI (American Megatrends, Inc.), Phoenix Technologies, Byosoft (Nanjing Byosoft Co., Ltd.) e Insyde Software.

Una actualización del BIOS normalmente implica eliminar todo el software del BIOS y la configuración almacenada en el CMOS. Algunos fabricantes proporcionan utilidades que te permiten guardar la configuración actual del CMOS antes de actualizar el BIOS. Siempre que sea posible, deben hacerse dos cosas antes de actualizar el flash BIOS: hacer una copia de seguridad de la configuración actual del CMOS y hacer una copia de seguridad del BIOS actual.

### UEFI

**Unified Extensible Firmware Interface (UEFI)** es la interfaz entre el sistema operativo y el firmware, que puede ser el BIOS tradicional, o UEFI puede reemplazar al BIOS. El BIOS tradicional siempre comprueba ciertas cosas, como un teclado, antes de permitir que el sistema arranque. El BIOS tradicional dificultaba la configuración de kioscos y otras tecnologías de pantalla táctil. UEFI solucionó estos problemas.

Con UEFI, puedes arrancar en un entorno especial. Muchos fabricantes se han pasado al tipo de BIOS UEFI por las siguientes razones:

- Es un entorno gráfico que brinda soporte para ratón.
- Te permite usar una utilidad de análisis de virus que no depende del sistema operativo.
- Ofrece software que no son solo pantallas de configuración.
- Ofrece acceso opcional a internet para solución de problemas o capacidades de descarga.
- Ofrece mejor soporte del sistema para enfriamiento, niveles de voltaje, rendimiento y seguridad.
- Proporciona soporte para mayores capacidades de disco duro y la capacidad de dividir el disco duro en secciones que no están sujetas a las limitaciones del BIOS tradicional.
- Comúnmente tiene datos relacionados con temperatura, voltaje, velocidad de la CPU, velocidad del bus y velocidad del ventilador.
- Puede tener un administrador de arranque en lugar de depender de un sector de arranque. Consulta el Capítulo 7, «Dispositivos de almacenamiento», para más información sobre la tabla de particiones GUID (GPT) y el sector de arranque. La Figura 4.3 muestra un ejemplo de un entorno UEFI.

> Figura 4.3 Menú principal de ejemplo de UEFI

Desde el menú principal del BIOS/UEFI, puede haber íconos que puedes usar para acceder a utilidades o a configuraciones más avanzadas, como se muestra en la Figura 4.4.

> Figura 4.4 Menú avanzado de ejemplo de UEFI

## Configuración de BIOS/UEFI

Las opciones del BIOS/UEFI varían según el fabricante, pero muchas opciones son similares. La Tabla 4.1 muestra algunos ajustes comunes y explica brevemente cada uno. Ten en cuenta que los elementos que son términos clave están en el examen de certificación CompTIA A+. Un técnico debe estar familiarizado con estas opciones comunes de Setup del BIOS/UEFI, especialmente con las opciones de seguridad marcadas con asterisco.

> Tabla 4.1 Opciones comunes de Setup del BIOS/UEFI

| Opción de Setup | Descripción |
|---|---|
| System Information | Muestra información general, como el procesador, la velocidad del procesador, la cantidad de RAM, el tipo y la cantidad de discos duros y unidades ópticas instalados, el fabricante del BIOS/UEFI y la fecha del BIOS/UEFI. |
| General Optimization | Permite un arranque más rápido al deshabilitar funciones como la comprobación de memoria, el arranque desde la red y el arranque desde unidades extraíbles. |
| Boot Options, Boot Sequence, Boot Drive Order o Boot Menu | Prioriza los dispositivos en el orden en que la computadora busca un sistema operativo. Se cambia cuando un sistema intenta arrancar desde un dispositivo incorrecto. |
| CPU Configuration o Advanced CPU Settings | Contiene ajustes como la función CPU TM, que afecta la gestión del límite de la CPU (ralentizarla cuando se sobrecalienta); la velocidad de reloj, que puede no ser modificable; PECI (Platform Environment Control Interface), que afecta cómo los sensores térmicos informan la temperatura del núcleo de la CPU; Max CPUID, que se usa para compatibilidad con sistemas operativos más antiguos; el control de CPU Ratio, que establece los multiplicadores de la CPU; y Vanderpool Technology, que se usa con la virtualización de Intel. |
| Fan Control | Permite la configuración de los ventiladores del gabinete y/o de la CPU, incluida la capacidad de poner los ventiladores en modo silencioso o controlar la velocidad del ventilador. |
| Video Options | Permite configuraciones como DVMT (dynamic video memory technology) para controlar la memoria de video, el tamaño de apertura (la cantidad de RAM del sistema dedicada al uso del adaptador de video) y qué controlador de video es primario o secundario. |
| Onboard Device Configuration | Permite modificar los dispositivos integrados en la placa madre, como audio, Bluetooth inalámbrico, red, USB o puertos de video. |
| * Passwords, Boot Password, Power on Password, Password Options, Supervisor Password, Administrator Password o User Password | Permite proteger las opciones del menú del BIOS/UEFI; específicamente, configurar una contraseña para entrar al programa Setup, para permitir que la computadora arranque o para distinguir entre alguien que puede hacer cambios menores, como alteraciones en las opciones de arranque o la fecha y hora (contraseña de usuario), o alguien que puede ver y cambiar todas las opciones de Setup (contraseña de supervisor o administrador). Otros fabricantes pueden tener los siguientes niveles: acceso completo (todas las pantallas excepto la contraseña de supervisor), acceso limitado, acceso de solo lectura o sin acceso. |
| * Virus Protection | Ejecuta una pequeña aplicación de análisis de virus ubicada en el BIOS/UEFI. Algunos sistemas operativos y actualizaciones de software requieren que esta opción esté deshabilitada para que la actualización proceda. |
| Numlock On/Off | Permite el ajuste predeterminado (habilitado o deshabilitado) de la opción de la tecla Bloq Num después del arranque. |
| USB Permissions | Permite modificar las opciones de velocidad USB y la cantidad de puertos a habilitar. |
| Hyper-Threading | Permite habilitar/deshabilitar la tecnología Hyper-Threading. |
| Integrated Peripherals (habilitar/deshabilitar dispositivos y puertos) | Permite habilitar/deshabilitar y configurar los dispositivos controlados por la placa madre, como los puertos PATA/SATA y los puertos integrados, incluidos USB, audio y red. Establece la cantidad de RAM dedicada al uso de video. Si la computadora tiene una cantidad abundante de RAM, aumentar este ajuste puede mejorar el rendimiento, especialmente en aplicaciones (como juegos) que usan gráficos de alta definición. |
| Advanced BIOS Options | Permite configurar opciones como las frecuencias de CPU y memoria, la CPU, el front side bus, el north bridge, el south bridge, el chipset y los niveles de voltaje de la memoria. |
| Interface Configurations | Indica una categoría o enumera una interfaz individual (por ejemplo, IDE Configuration, SATA Configuration, PCI Configuration, PCIe Configuration). |
| IDE Configuration | Permite la configuración manual de dispositivos IDE, como PATA, discos duros y unidades ópticas. |
| SATA Configuration | Permite ver los valores de Serial ATA asignados por el BIOS/UEFI y cambiar algunas de las opciones relacionadas, así como la configuración de RAID. |
| PCI/PnP Configuration | Permite ver y cambiar la configuración de las ranuras PCI, incluidas las asignaciones de IRQ y DMA. |
| PCIe Configuration | Permite la configuración manual de la versión de PCIe. |
| Devices | Permite configurar USB, SATA, video, dispositivos integrados y PCI, donde puede que sea necesario habilitar la ranura M.2 para que se reconozca el SSD. |
| Virtualization Support, Virtualization Technology o Secure Virtual Machine Mode | Habilita/deshabilita la virtualización para que el software de virtualización pueda acceder a capacidades de hardware adicionales. |
| ACPI (Advanced Configuration and Power Interface) | Determina qué ocurre si se pierde la energía, las opciones de energía si entra una llamada a un módem y las opciones de energía cuando lo indica un dispositivo PCI o PCIe o una acción del ratón/teclado. |
| Hardware Monitor | Permite ver el monitoreo de temperatura de la CPU y la placa madre, así como el estado de la CPU, el chasis, los voltajes, las velocidades de reloj, las velocidades de ventilador, las velocidades de bus, la detección/notificación de intrusión en el chasis y los ventiladores de la fuente de alimentación. |
| * Disable Execute Bit, Execute Disable o No Execute | Evita que se ejecute código ejecutable (virus) desde un área de memoria marcada específica. |
| * Drive Encryption | Especifica que se usa una clave secreta para cifrar los datos del disco duro. La computadora no arrancará sin la contraseña correcta. La unidad no se puede mover a otra computadora a menos que se introduzca la contraseña correcta. |
| * LoJack | Permite que la configuración de seguridad realice tareas como localizar el dispositivo, bloquearlo de forma remota, mostrar un mensaje de "si se pierde" o borrar datos si es robado. |
| * Intrusion Detection/Notification o Chassis Intrusion | Permite notificar si se ha quitado la cubierta. |
| * Secure Boot | Comprueba cada controlador antes de lanzar los controladores y el sistema operativo. Evita que un sistema operativo o software no autorizado se cargue durante el proceso de arranque. |
| iGPU | Permite configurar cuánta memoria se asigna a la GPU integrada. |
| Built-in Diagnostics | Proporciona acceso a los componentes de hardware, el disco duro, la memoria, la batería y otras pruebas de diagnóstico. |
| * Trusted Platform Module (TPM) | También puede aparecer como una opción PTT. Permite habilitar el chip TPM de la placa madre que genera y almacena claves y contraseñas criptográficas. También puedes borrar los datos guardados con la opción TPM Clear. Ten en cuenta que también puedes ver una opción fTPM (firmware TPM) si la función TPM usa la CPU y no un chip separado para proporcionar esta función. |
| * Opciones de seguridad | — |

### Consejo técnico: usar Setup para deshabilitar puertos y conectores

Las placas madre incluyen conectores para discos duros, unidades ópticas, etc. Si uno de estos conectores falla, puedes deshabilitarlo a través de Setup y obtener un adaptador de reemplazo tal como lo harías si fallara un puerto integrado. Setup también se puede usar para deshabilitar los puertos integrados de la placa madre.

### Consejo técnico: el sistema arranca desde el dispositivo incorrecto

Si una computadora intenta arrancar desde el dispositivo incorrecto, cambia el ajuste Boot Sequence (secuencia de arranque) en el BIOS/UEFI. También es posible que haya un disco óptico en la unidad o una unidad USB no arrancable conectada, y que sea esa la primera opción de arranque seleccionada actualmente.

La Figura 4.5 muestra una pantalla de ejemplo del BIOS/UEFI donde puedes establecer la contraseña de administrador o de usuario. Ten en cuenta que esta no es una contraseña de Windows ni de una red corporativa.

> Figura 4.5 Menú de seguridad de contraseñas

Debes guardar los cambios cada vez que realices cambios de configuración. Algunos fabricantes permiten guardar capturas de pantalla en una unidad flash USB. Salir sin guardar los cambios es un error común. La Tabla 4.2 enumera opciones de ejemplo para salir del BIOS/UEFI.

> Tabla 4.2 Opciones de ejemplo para cambios de configuración

| Opción | Descripción |
|---|---|
| Save & Exit Setup | Guarda todos los cambios y abandona el programa Setup. |
| Exit Without Saving | Cierra sin guardar ningún cambio realizado. Se usa cuando se han hecho cambios por error o se necesita más investigación. |
| Load Fail-Safe Defaults | Establece la configuración predeterminada programada por el fabricante. Se usa cuando ocurren resultados impredecibles tras cambiar una opción. |
| Load Optimized Defaults | Tiene ajustes más agresivos que la opción Load Fail-Safe Defaults. Esta opción está programada por el fabricante. |

### Consideraciones sobre TPM

El TPM viene en dos versiones principales: 1.2 y 2.0. La versión 2.0 es un estándar mundial, pero las opciones de UEFI de cada fabricante de computadoras podrían aparecer de forma diferente. Cuando habilitas el TPM a través del UEFI, seleccionas y habilitas el módulo TPM, que puede ser un módulo físico o hacerse a través del firmware. También puedes borrar el TPM.

### Consejo técnico: borrar el TPM invalida las claves de seguridad y causa pérdida de datos

Si borras el TPM, el TPM se apaga y todas las claves de seguridad existentes se invalidan, y esto puede causar la pérdida de acceso a datos cifrados. Asegúrate de que todos los datos estén respaldados antes de borrar el TPM. Puedes conservar todas las claves de seguridad y los datos si simplemente deshabilitas (apagas) el TPM en lugar de borrarlo.

En una computadora Windows, cada componente se comprueba en busca de controladores de arranque, rootkits y malware, y el TPM almacena esta información. La opción Secure Boot del UEFI, el cifrado de unidad BitLocker y Windows Defender hacen uso del TPM. Una vez que el TPM está habilitado, puedes iniciar el asistente de inicialización del TPM escribiendo tpm.msc en el cuadro de texto de búsqueda de Windows. Se te pedirá que crees una contraseña de propietario del TPM. Esta contraseña se puede guardar en medios extraíbles y/o imprimir. Ten en cuenta que esta es información muy importante y no se puede recuperar.

## Memoria CMOS

Los ajustes modificados en el BIOS/UEFI del sistema se registran y almacenan en un **semiconductor de óxido metálico complementario (CMOS)** que se encuentra en el chipset de la placa madre. El CMOS es memoria que requiere una pequeña cantidad de energía proporcionada por una batería de litio del tamaño de una moneda (batería CMOS) cuando el sistema está apagado. La memoria contiene los ajustes configurados a través del BIOS/UEFI. Cuando la batería se agota, toda la información de configuración del CMOS se pierde y debe volverse a introducir o reaprender después de reemplazar la batería.

### Consejo técnico: información incorrecta en Setup causa errores de POST

Si introduces información de configuración incorrecta, aparecen códigos de error de POST o mensajes de error que normalmente indicarían un problema de hardware.

## Batería de la placa madre

La batería CMOS más común que se usa hoy es una batería de litio CR2032, que es aproximadamente del tamaño de una moneda. La Figura 4.6 muestra una foto de una batería de litio instalada en una placa madre.

> Figura 4.6 Batería de la placa madre

### Consejo técnico: fecha, hora o ajustes restablecidos

Una primera indicación de que una batería está fallando es la fecha/hora del sistema inexacta en la computadora.

Ninguna batería dura para siempre. Las temperaturas altas acortan la vida útil de una batería (que normalmente es de tres a ocho años).

### Consejo técnico: usar un programa de reciclaje de baterías

Muchos estados tienen regulaciones ambientales sobre la eliminación de baterías. Muchas empresas también tienen programas de reciclaje de baterías. El sitio web earth911.com proporciona información sobre el reciclaje y la eliminación de baterías y componentes de computadora por código postal o ciudad/estado.

## Actualizaciones de firmware: flashear/limpiar el BIOS/UEFI

Las actualizaciones de firmware son necesarias para obtener nuevas funciones y abordar fallas de seguridad que puedan surgir. Los términos usados para este proceso son "flashear el BIOS" y "actualizar o mejorar el firmware". Una computadora puede necesitar una actualización del BIOS/UEFI por diversas razones, entre ellas las siguientes:

- Proporcionar soporte para hardware nuevo o actualizado, como un procesador o un puerto USB más rápido
- Proporcionar soporte para un disco duro de mayor capacidad
- Para mayor protección contra virus
- Para protección opcional con contraseña
- Para resolver problemas con la versión actual
- Para proporcionar un parche de seguridad

Los virus pueden infectar el BIOS/UEFI, así que debes mantener el BIOS protegido contra escritura hasta que necesites actualizarlo. El siguiente procedimiento es un ejemplo de cómo flashear el BIOS/UEFI:

Paso 1. Después de descargar la actualización del BIOS/UEFI del sistema desde internet, ejecuta la actualización haciendo doble clic en el nombre del archivo.

Paso 2. Sigue las instrucciones en pantalla o del fabricante.

Paso 3. Reinicia la computadora.

A veces, es posible que necesites restablecer el BIOS, y hay cuatro formas comunes de hacerlo: puente CMOS (*jumper*), botón de reinicio del CMOS, quitar la batería del CMOS, ajuste del BIOS/UEFI para restablecer a los valores predeterminados de fábrica. Un puente es una pequeña pieza de plástico que se ajusta sobre los pines. Un puente se puede usar para habilitar o deshabilitar una función en particular. La Figura 4.7 muestra un puente ampliado y un puente de contraseña del CMOS. La Figura 4.8 muestra un botón de reinicio del CMOS.

> Figura 4.7 Bloque de puentes JP1 con los pines 1 y 2 conectados entre sí, y puente de contraseña del CMOS

> Figura 4.8 Botón de reinicio del CMOS

### Consejo técnico: no limpiar el CMOS después de una actualización del BIOS/UEFI

No limpies el CMOS inmediatamente después de actualizar el BIOS/UEFI. Apaga el sistema y vuelve a encenderlo antes de limpiar los datos del CMOS.

Si vas a flashear el BIOS/UEFI de una laptop, asegúrate de que la batería de la laptop esté completamente cargada o, mejor aún, conecta la laptop a la corriente alterna. Si el BIOS se descarga (y no se guarda localmente), conecta la laptop a una red cableada para hacer la descarga y garantizar la conectividad durante el proceso de descarga.

Ten en cuenta que no todos los proveedores ofrecen un método para recuperar un BIOS/UEFI si una actualización por flash no sale bien. Una computadora sin un BIOS/UEFI operativo no puede arrancar, y hay que comprar una placa madre nueva. Por lo tanto, deberías tener una buena razón para flashear el BIOS/UEFI e investigar el método de respaldo que usa la placa madre antes de flashear el BIOS/UEFI.

## Otros parámetros de configuración

Otros parámetros posibles contenidos y establecidos mediante el programa Setup o el sistema operativo son las **solicitudes de interrupción (IRQ)**, las **direcciones de entrada/salida (E/S)**, los **canales de acceso directo a memoria (DMA)** y las **direcciones de memoria**. Estos parámetros se asignan a los adaptadores y puertos. Sin importar cómo se asignen los parámetros, en conjunto se conocen como **recursos del sistema**. Veamos las IRQ, las direcciones de E/S y las direcciones de memoria. La Tabla 4.3 describe brevemente estos recursos.

> Tabla 4.3 Recursos del sistema

| Tipo | Descripción |
|---|---|
| IRQ | Un número asignado a un adaptador, un puerto o un dispositivo para que pueda ocurrir una comunicación ordenada entre este y el procesador. Por ejemplo, cuando se presiona una tecla al mismo tiempo que se mueve el ratón, el teclado tiene la prioridad más alta debido a su número de IRQ. |
| Dirección de E/S | Una dirección única que permite a un adaptador, un puerto o un dispositivo intercambiar datos con un procesador. Estas direcciones permiten al procesador distinguir entre los dispositivos con los que se comunica. |
| Dirección de memoria | Una dirección única asignada a un chip de memoria instalado en cualquier parte del sistema. La CPU usa estas direcciones cuando accede a información dentro del chip de memoria. |

### IRQ

Imagina estar en una sala con 20 estudiantes cuando 4 estudiantes quieren la atención del maestro. El maestro necesita un proceso ordenado para reconocer cada solicitud, priorizar las solicitudes (qué estudiante va primero) y luego responder cada pregunta. Surge una situación similar cuando varios dispositivos quieren la atención de la CPU. Por ejemplo, ¿qué dispositivo pasa primero si se presiona una tecla del teclado y se mueve el ratón USB simultáneamente? La respuesta está en la solicitud de interrupción asignada al teclado y al ratón. Cada dispositivo solicita permiso para hacer algo interrumpiendo al procesador (lo que es similar a un estudiante levantando la mano). La CPU tiene un sistema de prioridades para manejar tales situaciones.

### Consejo técnico: cómo se asignan las IRQ a los puertos de múltiples dispositivos

Los puertos como USB que admiten varios dispositivos requieren solo una interrupción por puerto. Por ejemplo, un solo puerto USB puede admitir hasta 127 dispositivos pero solo necesita una IRQ para todos los dispositivos que se conecten a un concentrador USB.

Las interrupciones de adaptadores y dispositivos se ven y se establecen usando el **Administrador de dispositivos** en Windows o usando varios Paneles de control. Los técnicos necesitan saber cómo usar el Administrador de dispositivos, que muestra el estado del hardware instalado. Estas son las distintas formas de acceder al Administrador de dispositivos:

- Escribe devmgmt.msc desde un símbolo del sistema o el cuadro de texto de búsqueda.
- Escribe administrador de dispositivos desde el cuadro de texto de búsqueda en la barra de tareas.
- Selecciona Configuración > escribe administrador de dispositivos en el cuadro de búsqueda Buscar un ajuste.
- Selecciona el Panel de control Dispositivos e impresoras > vínculo Administrador de dispositivos.
- Selecciona el Panel de control Sistema y seguridad > Herramientas administrativas > Administración de equipos > Administrador de dispositivos.
- Haz clic con el botón derecho en el botón Inicio > Administrador de dispositivos.

Dentro del Administrador de dispositivos, selecciona Ver > Recursos por tipo y expande la sección Solicitud de interrupción (IRQ). Algunas interrupciones tienen varias entradas. Las entradas múltiples no siempre indican un conflicto de recursos; se permiten porque los dispositivos pueden compartir IRQ.

Para acceder a los detalles en el Administrador de dispositivos, usa la opción Ver > Dispositivos por tipo. Luego expande cualquier sección específica, como Adaptadores de red, haz clic con el botón derecho en un dispositivo o adaptador en particular y selecciona Propiedades. La Figura 4.9 muestra las propiedades de una tarjeta de red integrada, que no se pueden cambiar a través del Administrador de dispositivos, como lo indica el botón Cambiar configuración que aparece atenuado. (Sin embargo, las propiedades podrían modificarse a través del programa Setup del BIOS/UEFI del sistema.)

> Figura 4.9 Pestaña Recursos en el Administrador de dispositivos

### Consejo técnico: qué hacer cuando ocurre un conflicto

Si sospechas de un conflicto de recursos con una tarjeta, reinicia la computadora. El BIOS/UEFI y el sistema operativo tratarán de resolverlo. Esto puede requerir varios reinicios. Además, si hay un adaptador instalado, moverlo a otra ranura puede resolver la situación.

### Direcciones de E/S (entrada/salida)

Una **dirección de E/S**, también conocida como dirección de entrada/salida o dirección de puerto, permite a un dispositivo y a un procesador intercambiar datos. Una dirección de E/S es como un número de buzón; debe ser única. Las direcciones de E/S son simplemente direcciones que el procesador puede usar para distinguir entre los dispositivos con los que se comunica.

### Consejo técnico: ¿cuándo se necesita una dirección de E/S?

Recuerda que cada dispositivo debe tener una dirección de E/S separada. De lo contrario, la CPU no puede distinguir entre los dispositivos instalados.

Las direcciones de E/S se muestran en formato hexadecimal (base 16), de 0000 a FFFF. Algunas salidas se muestran con ocho posiciones, como de 00000000 a FFFFFFFF. Los números hexadecimales son 0, 1, 2, 3, 4, 5, 6, 7, 8 y 9, así como las letras A, B, C, D, E y F. Un ejemplo de dirección de E/S es 390h. Normalmente, los dispositivos necesitan más de una ubicación de dirección hexadecimal.

### Direcciones de memoria

Una **dirección de memoria** es una dirección única asignada a un chip de memoria instalado en cualquier parte del sistema. La CPU usa una dirección de memoria cuando accede a información dentro del chip. Las direcciones de memoria se muestran como un rango de direcciones hexadecimales en el Administrador de dispositivos (ver la Figura 4.10).

> Figura 4.10 Direcciones de memoria en el Administrador de dispositivos

## Descripción general de la configuración de hardware

La configuración de adaptadores y otro hardware es fácil si sigues la documentación y sabes cómo obtener los controladores de dispositivo. La documentación para la instalación con frecuencia está disponible en internet, al igual que muchos controladores de dispositivo. Los controladores de dispositivo también se proporcionan como parte del proceso de actualización de Windows.

El BIOS/UEFI del sistema desempeña un papel importante como parte de la rutina de inicio. No solo comprueba el hardware en busca de errores como parte de POST, sino que también detecta los adaptadores y dispositivos instalados. El BIOS/UEFI, junto con el sistema operativo, determina qué recursos asignar a un dispositivo o adaptador. Esta información se almacena en una parte del CMOS conocida como área **Extended System Configuration Data (ESCD)**. Una vez que la información se configura en el área ESCD, permanece allí y no tiene que volver a calcularse a menos que se agregue otro dispositivo.

Después de que se asignan los recursos, el BIOS busca en la configuración guardada del CMOS para determinar qué dispositivo debe consultar primero en busca de un sistema operativo. Esta parte de la rutina del BIOS/UEFI se conoce como **cargador de arranque** (*bootstrap loader*). Si el BIOS/UEFI no puede localizar un sistema operativo en la primera ubicación especificada en la configuración guardada, prueba el segundo dispositivo y continúa, buscando un sistema operativo en cada dispositivo especificado en la configuración guardada. Cuando se encuentra un sistema operativo, este se carga.

### Instalación de controladores

Al instalar hardware o un adaptador en el entorno Windows, se requiere un controlador. Recuerda que un controlador es software que permite al sistema operativo controlar el hardware. El sistema operativo detecta la instalación del adaptador o hardware y agrega la información de configuración del dispositivo al registro. El **registro** (*registry*) es una base de datos central en Windows que contiene información de hardware y otros datos. Todas las aplicaciones de software acceden al registro para obtener información de configuración en lugar de ir al adaptador.

Windows viene con muchos controladores para dispositivos comunes como teclados, ratones, impresoras y pantallas. Estos son algunos procesos usados para instalar un controlador:

- Puede que se te solicite instalar o buscar el controlador como parte del proceso de instalación. Es posible que debas indicar dónde se encuentra el controlador, como en un medio que viene con el hardware. También es posible que se te pida descargarlo e indicar dónde se encuentra el archivo descargado.
- Usa el Administrador de dispositivos para instalar un controlador. Abre el Administrador de dispositivos > expande la categoría de hardware relevante en particular > haz clic con el botón derecho en el dispositivo > Actualizar software de controlador, como se muestra en la Figura 4.11.

> Figura 4.11 Opción Actualizar software de controlador en el Administrador de dispositivos

- Usa el Explorador de archivos para localizar un archivo ejecutable que viene con el hardware. Haz doble clic en el archivo Setup proporcionado para instalar el software y/o un controlador.
- Usa la opción de Panel de control Agregar un dispositivo o el vínculo de Configuración Agregar Bluetooth u otro dispositivo (Windows 10)/Agregar un dispositivo (Windows 11).
- Usa el Asistente para agregar hardware escribiendo hdwwiz en el cuadro de texto de búsqueda de Windows.

## Instalación de un dispositivo USB

Para instalar un dispositivo USB, realiza los siguientes pasos:

Paso 1. Enciende la computadora.

Paso 2. Opcionalmente, instala el software del dispositivo USB. Ten en cuenta que algunos fabricantes requieren que el software y/o los controladores del dispositivo se instalen antes de conectar el dispositivo USB.

Paso 3. Opcionalmente, enciende el dispositivo. No todos los dispositivos USB tienen adaptadores de alimentación externos o un botón de encendido, porque reciben energía del bus USB.

Paso 4. Localiza un puerto USB en la parte trasera o frontal de la computadora o en un concentrador USB. Conecta el dispositivo USB en un puerto libre. El sistema operativo normalmente detecta el dispositivo USB y carga el controlador del dispositivo. Es posible que tengas que buscar el controlador.

Paso 5. Verifica la instalación en el Administrador de dispositivos.

### Consejo técnico: ignorar las recomendaciones del fabricante te trae problemas

Si un fabricante recomienda instalar el controlador del dispositivo antes de conectar el dispositivo USB, ¡sigue las instrucciones! No hacerlo puede requerir la desinstalación del controlador y luego la reinstalación usando los procedimientos recomendados, para que el dispositivo funcione correctamente.

### Instalación/configuración de tarjetas USB

Se pueden agregar puertos USB adicionales usando un concentrador USB o conectando una tarjeta de expansión USB, que es una placa metálica que tiene puertos USB adicionales que se conectan a los pines de la placa madre. La placa se inserta donde va una tarjeta de expansión, pero no tiene conectores que encajen en una ranura de expansión. La placa metálica simplemente se desliza en el lugar donde normalmente iría una tarjeta. La Figura 4.12 muestra una de estas placas; esta tiene dos puertos USB y un puerto eSATA. También puedes revisar la Figura 2.20 para ver cómo conectar los cables a la placa madre.

> Figura 4.12 Soporte/puertos USB y eSATA que se conectan a los pines de la placa madre

Ten en cuenta que si una placa madre no tiene pines, puedes agregar más puertos USB comprando un adaptador USB PCI o PCIe con varios puertos. Es posible que el adaptador no tenga la capacidad de proporcionar energía a menos que admita tener un cable de alimentación de la fuente de alimentación conectado a la tarjeta.

Es posible instalar una tarjeta USB para agregar puertos USB adicionales a una computadora. Los puertos USB reciben energía; por lo tanto, una tarjeta USB normalmente tiene un lugar para conectar la alimentación. Si la fuente de alimentación no tiene el conector de energía adecuado, es posible que haya que comprar un adaptador de energía. A continuación se presentan instrucciones genéricas:

Paso 1. Apaga la computadora y quita el cable de alimentación.

Paso 2. Quita la cubierta de la computadora. Localiza una ranura de expansión vacía. Es posible que tengas que quitar un tornillo o levantar una barra de retención para poder usar la ranura de expansión (ver la Figura 4.13).

> Figura 4.13 Tornillo del adaptador o barra de retención

Paso 3. Usando procedimientos antiestáticos adecuados (ver el Capítulo 5, «Desmontaje y energía»), conéctate a tierra o usa guantes antiestáticos.

Paso 4. Agrega un cable a la placa madre si usas un soporte USB. Opcionalmente, conecta un conector de energía al adaptador.

Paso 5. Asegúrate de que se use la ranura de expansión adecuada e inserta la tarjeta firmemente en la ranura (ver la Figura 4.14). Asegúrate de que la tarjeta esté completamente insertada presionando firmemente hacia abajo sobre el adaptador e inspeccionándolo visualmente después. La tarjeta debe estar en un ángulo de 90 grados respecto de la PC. No debe inclinarse en ninguno de sus extremos. Asegúrate de que la tarjeta encaje bien en la ranura de expansión.

> Figura 4.14 Inserción de un adaptador directamente en una ranura de expansión

Paso 6. Baja la barra de expansión o coloca un tornillo, si es necesario.

Paso 7. Vuelve a instalar la cubierta de la computadora, vuelve a conectar el cable de alimentación y enciende la computadora. Instala los controladores según sea necesario.

Paso 8. Prueba conectando un dispositivo USB a cada puerto.

### Solución de problemas de USB

Para solucionar problemas de dispositivos USB, comprueba primero lo obvio: el cableado y la energía. Verifica si funciona algún dispositivo USB que se conecte a un concentrador USB. Si ningún dispositivo funciona, cambia el concentrador o conéctalo a un puerto USB diferente. Si algunos puertos del concentrador funcionan y otros no, conecta una fuente de alimentación externa al concentrador, cambia su configuración si es necesario y vuelve a probar los dispositivos. Reinicia la computadora y vuelve a probar el dispositivo USB.

Los puertos USB pueden proporcionar energía a diferentes niveles, como 2 A a 5 V (10 W), 5 A a 12 V (60 W) y 5 A a 20 V (100 W). Tampoco todos los cables USB-C pueden proporcionar 100 W de energía. Asegúrate de usar un cable USB-C a USB-C con clasificación de 5 A.

Puedes verificar cuánta energía está usando un dispositivo USB usando software externo como USBDeview. Puedes ver el estado de energía usando el Administrador de dispositivos con estos pasos.

Paso 1. Expande la sección Controladoras de bus serie universal (USB).

Paso 2. Haz clic con el botón derecho en cada opción Concentrador USB genérico y selecciona Propiedades.

Paso 3. Accede a la pestaña Detalles y usa la flecha desplegable Propiedad para seleccionar Datos de energía.

Paso 4. En la sección Estado de energía actual, observa el estado de D0 a D3. Un estado D0 es el estado totalmente encendido y D3 es el estado de menor consumo de energía (modo de suspensión incluso si tiene dispositivos conectados).

Un dispositivo USB podría estar consumiendo más energía de la permitida. Si es el caso, la computadora puede deshabilitar el puerto. La única forma de volver a habilitar el puerto es reiniciar la computadora. Si un dispositivo usa menos de 50 mA de energía, el puerto USB nunca se activa. Intenta conectar el dispositivo USB en un puerto USB diferente o verifica que el dispositivo funcione en otra computadora.

En Windows 10 y 11, en Propiedades del concentrador USB > pestaña Administración de energía, es posible permitir (ajuste predeterminado) o impedir que la computadora apague el puerto/concentrador USB para ahorrar energía (ver la Figura 4.15).

> Figura 4.15 Administración de energía de Windows para el puerto USB

Un dispositivo USB requiere un controlador que puede cargarse automáticamente. Se podría haber cargado un controlador incorrecto o desactualizado que esté causando problemas. La siguiente lista también puede ayudar al solucionar problemas de dispositivos USB:

- Usa el Administrador de dispositivos para asegurarte de que un concentrador funcione correctamente.
- Asegúrate de que el firmware del BIOS/UEFI esté actualizado.
- Usa el Administrador de dispositivos para asegurarte de que ningún dispositivo USB tenga asignada una IRQ y la comparta con otro dispositivo que no sea USB.
- Los dispositivos USB a veces no funcionan en modo seguro y requieren soporte de hardware configurado a través del BIOS/UEFI.
- A veces un dispositivo USB deja de funcionar en un concentrador que tiene una fuente de alimentación externa. En tal caso, quita la fuente de alimentación externa del concentrador y vuelve a probar.
- Si a un concentrador USB autoalimentado se le desconecta la energía, el concentrador se convierte en un concentrador alimentado por bus y emite solo menor energía en cada puerto. Vuelve a conectar el cable de alimentación o quita el concentrador y vuelve a conectarlo.
- Si un dispositivo USB recién conectado informa que está conectado pero no funciona correctamente, actualiza el controlador.
- No conectes dispositivos USB a una computadora que esté en modo de espera o de suspensión. Hacerlo puede impedir que la computadora salga del modo de espera.
- Para problemas intermitentes de dispositivos USB, deshabilita la administración de energía para ver si eso resuelve el problema.
- Prueba un dispositivo conectado a un concentrador USB conectándolo directamente a un puerto USB que no tenga nada más conectado. El problema puede deberse a otros dispositivos USB o a un concentrador USB.
- Quita el controlador del dispositivo USB y vuelve a instalarlo. A veces debes reiniciar la computadora para dar a los nuevos controladores prioridad sobre los controladores de uso general.
- Si un dispositivo USB funciona lentamente, intenta conectarlo a un puerto diferente que tenga menos dispositivos conectados al mismo puerto.
- Verifica que el puerto USB esté habilitado en el BIOS/UEFI si está integrado en la placa madre o conectado a la placa madre mediante un cable adaptador.
- Consulta el sitio web del fabricante del dispositivo USB para obtener detalles específicos de solución de problemas.

## Instalación de una tarjeta eSATA

Un puerto **Serial ATA (SATA)** permite la conexión de un dispositivo de almacenamiento SATA, como un disco duro o una unidad óptica. Los puertos **SATA externo (eSATA)** permiten la conectividad de dispositivos de almacenamiento fuera de la computadora o laptop. Si una computadora no tiene puertos eSATA o no tiene suficientes, existen dos opciones. La primera opción es que puedes instalar un soporte eSATA, como se muestra en la Figura 4.16. Observa que los cables SATA simplemente se conectan a la parte posterior de los puertos. Cada cable SATA se conecta a un puerto de la placa madre. Para el soporte mostrado, la placa madre necesita tener dos puertos SATA disponibles para tener dos puertos externos.

> Figura 4.16 Soporte eSATA con cables

La segunda opción es tener una tarjeta eSATA PCIe, como se muestra en la Figura 4.17. Observa que esta tarjeta no trae cables, como sí hace un soporte eSATA, y tiene puertos en la parte superior de la tarjeta además de los externos. Podrías conectar un cable SATA desde la parte superior de esta tarjeta a un dispositivo interno o conectar un cable eSATA desde uno de los puertos externos a un dispositivo eSATA externo.

> Figura 4.17 Tarjeta eSATA PCIe

Para instalar una tarjeta o soporte eSATA, realiza los siguientes pasos:

Paso 1. Apaga la computadora y desenchúfala.

Paso 2. Quita la cubierta de la computadora y localiza una ranura de expansión sin usar. Es posible que tengas que quitar un tornillo o levantar una barra de retención para poder usar la ranura de expansión.

Paso 3. Quita la cubierta de la ranura.

Paso 4. Usando procedimientos antiestáticos adecuados (ver el Capítulo 5, «Desmontaje y energía»), conéctate a tierra o usa guantes antiestáticos.

Paso 5. Asegúrate de que se use la ranura de expansión adecuada. Inserta la tarjeta firmemente en la ranura de expansión. Si solo se usa un soporte, insértalo entre la placa madre y la parte posterior del gabinete donde hay una ranura de expansión vacía.

Paso 6. Baja la barra de expansión o coloca un tornillo para mantener la tarjeta o el soporte firmemente en su lugar.

Paso 7. Si se usa un soporte, conecta cada cable SATA a un puerto SATA disponible de la placa madre. Toma nota de qué puerto SATA se usa, ya que cada uno puede necesitar habilitarse dentro del BIOS/UEFI.

Paso 8. Vuelve a instalar la cubierta de la computadora, vuelve a conectar el cable de alimentación y enciende la computadora. Entra al BIOS/UEFI y habilita los puertos SATA apropiados según sea necesario. Instala cualquier software que venga con la tarjeta.

Paso 9. Prueba conectando un dispositivo eSATA a cada puerto.

## Instalación de una tarjeta de interfaz de red

Casi todos los dispositivos se conectan a una red cableada o inalámbrica usando una **tarjeta de interfaz de red (NIC)**. Muchos dispositivos tienen NIC cableadas e inalámbricas integradas, pero si tal NIC falla, se debe instalar una NIC nueva, como la NIC Ethernet que se muestra en la Figura 4.18.

> Figura 4.18 Tarjeta de interfaz de red Ethernet

Debes seguir varios pasos como parte del proceso de instalación antes de conectarte a la red:

Paso 1. Determina que haya una ranura de expansión adecuada disponible.

Paso 2. Quita la cubierta de la computadora y localiza una ranura de expansión sin usar. Quita la cubierta de la ranura.

Paso 3. Conéctate a tierra y asegúrate de que se use la ranura de expansión adecuada. Inserta la tarjeta firmemente en la ranura de expansión. Asegura la tarjeta.

Paso 4. Vuelve a instalar la cubierta de la computadora, vuelve a conectar la energía y enciende la computadora. Descarga e instala el controlador más reciente.

Paso 5. Dale a la computadora un nombre único y, opcionalmente, únete a un grupo de trabajo o dominio.

Paso 6. Configura la información de direccionamiento TCP/IP, como se describe en el Capítulo 13, «Redes».

## Solución de problemas de configuraciones

Las siguientes son posibles indicaciones de que un dispositivo no funciona:

- Se instala un dispositivo nuevo, y el dispositivo nuevo o un dispositivo previamente instalado no funciona.
- La computadora se bloquea o se reinicia al realizar una función específica, como al reproducir o grabar audio.
- La computadora se cuelga durante el inicio o el apagado.
- Un dispositivo no funciona correctamente o no funciona en absoluto.

### Consejo técnico: verificar el hardware con el Administrador de dispositivos

Una pequeña flecha hacia abajo junto al ícono de un dispositivo en el Administrador de dispositivos significa que el dispositivo está deshabilitado, y un signo de exclamación (!) sobre un campo amarillo generalmente indica un conflicto de recursos o un problema de controlador. Una "i" indica que la función Usar configuración automática no se está usando para el dispositivo y que los recursos se configuraron manualmente.

En el Administrador de dispositivos, si aparece un signo de exclamación (!), el dispositivo de hardware no funciona correctamente y debes comprobar problemas de cableado, conflictos de recursos y problemas de configuración. Si aparece un signo de interrogación amarillo, Windows no reconoce el dispositivo, y puedes intentar una de las siguientes opciones:

- Realiza una actualización de Windows para asegurarte de tener los controladores, las actualizaciones de seguridad y las correcciones más recientes.
- Actualiza manualmente el controlador haciendo clic con el botón derecho en el dispositivo en el Administrador de dispositivos y seleccionando Propiedades > pestaña Controlador > Actualizar controlador. Puedes descargar este controlador del sitio web del fabricante del dispositivo o dejar que Windows intente encontrar el controlador.

### Consejo técnico: usar la pestaña General para la solución de problemas

En la pestaña General del cuadro de diálogo Propiedades de cualquier adaptador o puerto, comprueba la sección Estado del dispositivo en busca de códigos de error, incluidos los de conflictos de recursos.

Con cualquier problema del Administrador de dispositivos, puedes hacer clic con el botón derecho en el dispositivo y seleccionar Propiedades. Mira la pestaña General para ver si hay códigos de error.

Los problemas de configuración también pueden estar asociados con ajustes específicos del BIOS/UEFI. La Tabla 4.5 enumera algunos problemas y cómo podrías resolverlos.

> Tabla 4.5 Solución de problemas relacionados con el BIOS/UEFI

| Problema | Cosas que probar |
|---|---|
| Aparece un mensaje que indica que la fecha y la hora no están configuradas, que el reloj no está configurado, que todos los ajustes guardados del BIOS/UEFI se perdieron, o que ocurren problemas inesperados en más de una aplicación. | Comprueba la fecha y la hora a través del sistema operativo. Reemplaza la batería CMOS de la placa madre. |
| No se puede configurar un sistema para virtualización. | Habilita la virtualización en el BIOS/UEFI. |
| El dispositivo conectado no funciona. | Si el dispositivo se conecta a un puerto de la placa madre, asegúrate de que el puerto no esté deshabilitado en el BIOS/UEFI. Asegúrate de que el dispositivo se conecte al puerto correcto, incluido un posible puerto en un adaptador en lugar de en la placa madre. Si el dispositivo se conecta a un puerto de un adaptador del mismo tipo que uno de la placa madre, es posible que el puerto integrado deba deshabilitarse en el BIOS/UEFI. |
| El sistema se bloquea esporádicamente. | Si hay overclocking, devuelve el sistema a su configuración original. |
| El sistema tarda en arrancar o arranca desde el dispositivo incorrecto. | Comprueba el ajuste del orden de arranque del BIOS/UEFI. |

## Habilidades blandas: buena práctica de un técnico: cambia solo una cosa a la vez y documenta

El tipo menos eficaz de técnico de computadoras es un "pistolero". El término pistolero trae a la mente imágenes de matones del Viejo Oeste que tenían tiroteos con otros forajidos en la calle principal del pueblo. Los pistoleros desenfundaban sus armas con frecuencia y con poca provocación. No pensaban mucho en su método ni consideraban otras posibles soluciones. Debes esforzarte por no ser este tipo de técnico.

Un técnico pistolero cambia varias cosas simultáneamente. Por ejemplo, si no hay imagen en la salida, el técnico podría cambiar el monitor, deshabilitar el puerto de video integrado, agregar un nuevo adaptador de video, encender la computadora y, cuando aparece la imagen, dar el problema por "resuelto". Si un problema de computadora se repara usando tal técnica, el técnico nunca sabe exactamente qué lo resolvió. Un técnico pistolero puede frustrarse fácilmente porque es fácil olvidar lo que se ha probado cuando se han probado varias cosas simultáneamente, y es casi imposible saber cuál funcionó (ver la Figura 4.19).

> Figura 4.19 Un técnico "pistolero" en acción

Un buen técnico, en cambio, hace una lista de síntomas (aunque sea simplemente mental) seguida de una lista de cosas que probar. Luego el técnico prueba las posibles soluciones, empezando por la más simple (la que cuesta menos tiempo al usuario de la computadora). El técnico documenta cada paso. Después de cada enfoque que no resuelve el problema, el técnico devuelve el sistema a su configuración original antes de intentar la siguiente solución posible. Este método mantiene al técnico enfocado en lo que se ha probado, y si otro técnico toma el relevo, los pasos no tienen que repetirse. Lo mejor de todo es que, cuando una de las posibles soluciones resuelve el problema, se conoce la solución exacta.

Los técnicos pistoleros no aprenden tan rápido como otros técnicos porque no determinan las causas reales de los problemas. Cada vez que se les presenta un problema similar a uno que han visto en el pasado, los técnicos pistoleros usan el mismo método de solución de problemas desordenado. Estos técnicos son en realidad peligrosos para una organización porque no son buenos documentando lo que han hecho ni determinando exactamente qué soluciona un problema en particular. Un buen técnico de computadoras debe solucionar los problemas metódicamente haciendo solo un cambio a la vez y revirtiendo el cambio si este no resuelve el problema. Además, el técnico necesita documentar el problema y su resolución para problemas futuros.

## Resumen del capítulo

- El BIOS/UEFI se usa para habilitar/deshabilitar, configurar y solucionar problemas de componentes de la placa madre, ranuras de expansión y puertos, y establece las contraseñas de encendido y del BIOS/UEFI.
- Un tipo actualizado de BIOS es el BIOS/UEFI, que permite el uso de un ratón y un entorno gráfico. También puede incluir opciones de seguridad, soporte para discos duros más grandes, software antivirus, administración remota y utilidades.
- Cuando una computadora está apagada, una batería de la placa madre mantiene los ajustes guardados en el CMOS. Si una computadora no conserva la fecha y la hora, reemplaza la batería.
- El TPM se puede habilitar o borrar a través del UEFI. Ten en cuenta que si borras el TPM, todos los certificados de seguridad digital, las contraseñas y los datos cifrados se pierden. Considera deshabilitar el TPM en su lugar.
- Cada puerto y tarjeta usa recursos del sistema, como interrupciones, direcciones de E/S y direcciones de memoria.
- Los recursos del sistema se pueden ver y cambiar usando el Administrador de dispositivos. También puedes usar el Administrador de dispositivos para ver que un dispositivo funcione correctamente.
- Se puede agregar una tarjeta USB, una tarjeta o soporte eSATA, o una NIC a una computadora para proporcionar puertos adicionales.

### Consejos para el examen de certificación A+

- Muchas preguntas de ambos exámenes pueden venir de este capítulo, especialmente en las áreas de solución de problemas. Revisa las viñetas de solución de problemas. Investiga los problemas en internet y lee las publicaciones de la gente. Sus historias y frustraciones (y éxitos) se te quedarán grabados y te ayudarán en el examen.
- Usando al menos una computadora, recorre los menús del BIOS/UEFI. Revisa qué tipos de cosas se pueden configurar a través del BIOS/UEFI. Los ajustes importantes incluyen los siguientes: opciones de arranque, ajustes USB, incluidos permisos y la capacidad de deshabilitar los puertos, opciones de ventilador, ajustes de seguridad (contraseñas, incluida una contraseña de arranque) y ajustes de TPM.
- Sé capaz de instalar y configurar una tarjeta de interfaz de red (NIC) y otros adaptadores.
- Saber qué hacer si un sistema intenta arrancar desde un dispositivo incorrecto o si la fecha/hora del sistema es incorrecta.

## Términos clave

- Contraseña de administrador — *Administrator Password*
- BIOS
- Contraseña de arranque — *boot password*
- Opciones de arranque — *Boot Options*
- CMOS
- Batería CMOS — *CMOS battery*
- Administrador de dispositivos — *Device Manager*
- Disable Execute Bit
- Cifrado de unidad — *Drive Encryption*
- Soporte eSATA — *eSATA bracket*
- Tarjeta eSATA — *eSATA card*
- ESCD
- Control de ventilador — *Fan Control*
- Actualización de firmware — *firmware update*
- Flashear el BIOS — *flash BIOS*
- fTPM
- Dirección de E/S — *I/O address*
- Fecha/hora del sistema inexacta — *inaccurate system date/time*
- Detección/notificación de intrusión — *Intrusion Detection/Notification*
- IRQ
- Puente — *jumper*
- LoJack
- Dirección de memoria — *memory address*
- NIC
- Contraseñas — *Passwords*
- POST
- Registro — *registry*
- Arranque seguro — *Secure Boot*
- Ajustes de seguridad — *security settings*
- Setup
- El sistema intenta arrancar desde un dispositivo incorrecto — *system attempts to boot to an incorrect device*
- Recursos del sistema — *system resources*
- TPM
- UEFI
- Tarjeta de expansión USB — *USB expansion card*
- Permisos USB — *USB Permissions*
- Soporte de virtualización — *Virtualization Support*

## Preguntas de repaso

1. ¿Cuándo flashearía un técnico el BIOS/UEFI?
   a. Cuando la fecha y la hora empiezan a ser incorrectas
   b. Cuando un puerto o componente de la placa madre no funciona a su máximo potencial
   c. Cuando el controlador de un puerto de la placa madre está desactualizado
   d. Cuando la placa madre tiene una actualización, como un nuevo procesador, RAM adicional o un adaptador adicional instalado en una ranura de expansión

2. ¿Cuál es el efecto de establecer una contraseña de administrador en el BIOS/UEFI?
   a. Evita que la computadora tenga varios dispositivos que puedan iniciar el sistema.
   b. Evita que el BIOS/UEFI se infecte con un virus.
   c. Evita que un usuario acceda al sistema operativo de la computadora.
   d. Evita que un usuario cambie la configuración de Setup del sistema.

3. ¿Qué programa se usa para determinar la versión del controlador que se usa para una tarjeta instalada en una computadora?
   [ BIOS | CMOS | Administrador de tareas | Administrador de dispositivos | System Setup ]

4. ¿Qué programa se usa comúnmente para verificar que el sistema operativo reconozca un nuevo componente de hardware, que funcione y los recursos del sistema asignados?
   [ BIOS/UEFI | CMOS | aplicación proporcionada por el fabricante | Administrador de dispositivos ]

5. ¿Dónde se usaría más probablemente una batería de litio CR2032 en una PC de torre?
   a. Como batería de Bluetooth
   b. Dentro del procesador
   c. Como componente de la placa madre
   d. En el CMOS

6. ¿Qué opción del BIOS/UEFI podría necesitar modificarse para arrancar una computadora Windows desde una unidad flash que contiene Ubuntu, un sistema operativo basado en Linux?
   [ LoJack | Secure Boot | Protección contra virus | Configuración USB | Hyper-Threading ]

7. ¿Qué es un TPM?
   a. Un método para compartir recursos entre adaptadores
   b. Un módulo físico que almacena contraseñas y certificados digitales
   c. La técnica usada por un concentrador USB cuando se conectan varios dispositivos
   d. Un tipo de batería de litio usada para mantener los datos de configuración actuales de Setup

8. Un técnico está revisando una computadora usada que alguien compró recientemente, y la computadora solicita una contraseña antes de que se cargue el sistema operativo. ¿Qué puede hacer el técnico para quitar la contraseña?
   a. Presionar la tecla para entrar al BIOS
   b. Presionar la tecla F8 mientras arranca la computadora
   c. Quitar la batería CMOS durante un minuto y luego reinstalarla
   d. Mantener presionado el botón de encendido durante 10 segundos mientras arranca la computadora

9. ¿Qué pestaña del cuadro de diálogo Propiedades de un dispositivo tiene una sección Estado del dispositivo que puede contener información útil para la solución de problemas o el estado del dispositivo?
   [ General | Avanzado | Controlador | Detalles | Administración ]

10. Un técnico recibe una queja sobre una computadora que responde lentamente a las pulsaciones de teclas. El técnico instala más memoria y un teclado nuevo. El cliente queda satisfecho. ¿Qué, si algo, podría haberse hecho mejor?

11. ¿Cuál es el vataje máximo que puede proporcionar un puerto USB?
   [ 100 | 5 | 2.5 | 4.5 ]

Para responder las preguntas 12 a 15, considera las siguientes opciones del menú de configuración del BIOS/UEFI.

12. ¿Qué menú usarías para determinar si el sistema debería flashearse?
   a. Menú principal (Main)
   b. Dispositivos integrados (Onboard Devices)
   c. Prioridad de dispositivo de arranque (Boot Device Priority)

13. Una computadora está montada dentro de un gabinete, y quieres saber si el puerto USB 3.0 ha sido deshabilitado. ¿Qué menú usarías?
   a. Menú principal (Main)
   b. Dispositivos integrados (Onboard Devices)
   c. Prioridad de dispositivo de arranque (Boot Device Priority)

14. ¿Qué menú usarías para determinar si el puerto SATA particular que usaste para conectar un soporte eSATA está habilitado?
   a. Menú principal (Main)
   b. Dispositivos integrados (Onboard Devices)
   c. Prioridad de dispositivo de arranque (Boot Device Priority)

15. Un técnico quiere arrancar desde un disco duro externo eSATA. ¿Qué elemento del submenú debería usar?
   [ Controlador SATA OnChip | SATA | PCIe Training | 1er dispositivo de arranque ]

16. Un técnico tiene que configurar la fecha y la hora repetidamente. ¿Qué componente es sospechoso?
   [ CPU | BIOS/UEFI | batería | chipset | CMOS ]

17. ¿Cuáles son tres formas de obtener más puertos USB? (Elige tres.)
   a. Conectar un concentrador USB a un puerto USB existente.
   b. Conectar un concentrador de red a un puerto USB existente.
   c. Instalar un adaptador PCIe que tenga puertos USB.
   d. Instalar un adaptador AGP que tenga puertos USB.
   e. Instalar un soporte USB que tenga puertos USB y se conecte a los pines de la placa madre.
   f. Usar un multiplexor de puertos USB.

18. ¿Cuándo usaría un técnico UEFI?
   a. Al gestionar la configuración mediante el Administrador de dispositivos
   b. Cuando la fecha y/o la hora siguen siendo incorrectas
   c. Cuando se acaba de instalar un adaptador
   d. Al reemplazar una placa madre

Nota del instructor: cuando se reemplaza una placa madre, deben realizarse las configuraciones de BIOS/UEFI.

19. Una computadora se usa en un consultorio médico. Por razones de seguridad, se le ha pedido al técnico que garantice razonablemente que nadie conecte ningún medio externo. ¿Qué haría probablemente el técnico?
   a. Proteger con contraseña el BIOS/UEFI y deshabilitar los puertos no usados.
   b. Cambiar la placa madre por una que no tenga puertos adicionales.
   c. Asignar derechos de usuario mediante contraseñas de usuario en la computadora.
   d. Cifrar el disco duro.
   e. Flashear el chipset.

20. Un técnico de una empresa pequeña estableció una contraseña de BIOS/UEFI en cada computadora. El técnico deja la empresa, y el técnico de reemplazo necesita acceder al BIOS/UEFI. ¿Qué debería hacer el nuevo técnico?

## Ejercicios

**Ejercicio 4.1 Expansión del sistema**

Objetivo:
 Poder explorar diferentes formas de expandir un sistema

Partes:
 Ninguna

Procedimiento: usa la documentación de la Tabla 4.6 para responder las preguntas.

> Tabla 4.6 Especificaciones de la placa madre

| Componente | Descripción |
|---|---|
| CPU | Soporte para Intel Celeron, Core i3 y Core i5 |
| Chipset | Intel B150 Express |
| Memoria | 2 zócalos DIMM DDR4 que admiten hasta 32 GB; soporte de doble canal; soporte para DDR4 a 2133 MHz |
| Gráficos integrados | Procesador de gráficos integrado; 2 puertos HDMI; memoria compartida máxima de 512 MB |
| Audio | Códec Realtek ALC887; 2/4/5.1/7.1 canales; soporte de salida S/PDIF |
| LAN | 2 chips Intel GbE LAN que admiten 10/100/1000 Mb/s |
| Ranuras de expansión | Ranura PCIe 3.0 x16; 1 conector M.2 Socket 1 para módulo inalámbrico |
| USB | Chipset: 4 puertos USB 2.0/1.1 (2 en la parte trasera y 2 a través de la cabecera USB interna); 6 puertos USB 3.0/2.0 (4 en la parte trasera y 2 a través de la cabecera USB interna) |
| Conectores internos | 1 conector de alimentación principal ATX de 24 pines; 1 conector de alimentación ATX de 4 pines y 12 V; 6 conectores SATA de 6 Gb/s; 1 conector M.2 Socket 3; 1 cabecera de ventilador de CPU; 1 cabecera de ventilador del sistema; 1 cabecera del panel frontal; 1 cabecera de audio del panel frontal; 1 cabecera USB 3.0/2.0; 1 cabecera USB 2.0/1.1; 4 cabeceras de puerto serie; 1 cabecera de salida S/PDIF; 1 cabecera de altavoz; 1 puente para borrar CMOS |
| Conectores del panel trasero | 2 puertos USB 2.0/1.1; 1 puerto de teclado/ratón PS/2; 2 conectores de antena Wi-Fi; 2 puertos HDMI; 4 puertos USB 3.0/2.0; 2 puertos RJ45; 6 tomas de audio |

1. La computadora que usa esta placa madre tiene un disco duro SATA conectado. El propietario de esta computadora quiere usar una unidad eSATA.
   Según la documentación proporcionada, ¿puede el usuario conectar una unidad eSATA a la computadora tal como está configurada ahora?
   [ Sí | No ]

2. El técnico quiere usar un soporte eSATA que tiene dos puertos/cables eSATA además de un dispositivo SATA interno.
   ¿Admite esto la placa madre? Explica cómo lo sabes.

3. Al usuario propietario de la computadora no le gusta usar concentradores USB.
   ¿Cuál es la cantidad máxima de dispositivos que el usuario puede conectar a la parte trasera de la computadora sin usar concentradores USB? ¿Qué consejo podrías darle al usuario respecto de estos puertos?

4. El usuario quiere puertos USB adicionales en la parte trasera de la computadora. Al técnico le gustaría usar un soporte USB para proporcionar dos puertos adicionales.
   Según la documentación, ¿se puede usar un soporte USB con esta placa madre? ¿Cómo puedes saberlo? Sé específico.

**Ejercicio 4.2 Opciones del BIOS/UEFI**

Objetivo:
 Usar la información que se encuentra en la pantalla del BIOS/UEFI para determinar qué opción usar

Partes:
 Ninguna

Procedimiento:
 Usa las Figuras 4.20 y 4.21 para responder las preguntas.

Usa la Figura 4.20 para responder las preguntas 1–5.

> Figura 4.20 Ventana de ejemplo del BIOS/UEFI 1

1. El usuario ha modificado las opciones del BIOS/UEFI hasta el punto de que la mitad de los puertos no funcionan y la computadora va lenta.
   ¿Qué opción de menú o tecla debería usar el técnico para resolver este problema?

2. El técnico ha modificado algunos ajustes, pero ahora quiere investigar algunas alternativas y no quiere conservar los ajustes que acaba de cambiar.
   ¿Qué opción de menú o tecla debería usar el técnico en esta situación?

3. Las computadoras del laboratorio de investigación deben tener seguridad adicional. Un técnico que configura una computadora nueva para ese laboratorio está usando el BIOS/UEFI para deshabilitar todos los puertos USB de los paneles frontal y trasero.
   ¿Qué opción de menú se usa para completar esta tarea?
   [ Main | Advanced | Monitor | Boot | Tools ]

4. El técnico quiere ver la última vez que alguien abrió el gabinete.
   ¿Qué opción de menú se usa para completar esta tarea?
   [ Main | Advanced | Monitor | Boot | Tools ]

5. El usuario se ha quejado de que el sistema tarda demasiado en arrancar. Algo que hizo un técnico anterior fue hacer que el sistema siempre intentara arrancar desde una unidad externa usada para reimagenar la computadora. Si no se encontraba la unidad externa, entonces usaba el disco duro interno para cargar el sistema operativo.
   ¿Qué opción de menú debería usar el nuevo técnico para cambiar el sistema y que use el disco duro interno para cargar el sistema operativo como primera opción de la computadora?
   [ Main | Advanced | Monitor | Boot | Tools ]

Usa la Figura 4.21 para responder las preguntas 6–10.

> Figura 4.21 Ventana de ejemplo del BIOS/UEFI 2

6. El técnico quiere impedir que el usuario cambie los ajustes del BIOS/UEFI.
   ¿Qué opción de menú o tecla debería usar el técnico para establecer una contraseña de administrador del BIOS/UEFI?
   [ Home | System Info | Peripherals | Power Management ]

7. Hace una semana, un usuario se quejó de que la hora de la computadora estaba mal. El técnico cambió la hora y la fecha. Ahora el usuario se ha quejado de nuevo de que la fecha y la hora son incorrectas. Si el técnico cambia la hora otra vez y comprueba la computadora al día siguiente y la encuentra mal de nuevo, ¿qué debería hacer el técnico?
   a. Flashear el BIOS/UEFI.
   b. Reemplazar la placa madre.
   c. Reemplazar la batería de la placa madre.
   d. Restablecer la hora por tercera vez.

8. Un jugador ha estado ajustando funciones de temporización en esta placa madre para acelerar el sistema.
   ¿Qué tecla podría usar el usuario para tomar una captura de pantalla de la configuración actual?
   F10

9. El técnico ha estado modificando ajustes del BIOS/UEFI.
   ¿Qué tecla debería usar el técnico al salir de la pantalla de Setup?
   F9

10. El técnico quiere habilitar dos puertos SATA para que un soporte eSATA de dos puertos pueda conectarse a la placa madre.
    ¿Qué opción de menú debería usar el técnico para asegurarse de que los dos puertos SATA estén habilitados?
    [ Home | System Info | Peripherals | Power Management ]

## Actividades

**Descubrimiento en internet**

Objetivo:
 Obtener información específica en internet sobre una computadora o sus partes asociadas

Partes:
 Computadora con acceso a internet

Procedimiento:
 Usa internet para responder las siguientes preguntas. Supón que el cliente posee una computadora todo-en-uno Asus M241 al responder las preguntas 1 y 2.

Preguntas:

1. Un cliente posee una computadora todo-en-uno Asus M241. Determina el procedimiento para acceder al programa Setup de la computadora. Escribe la(s) tecla(s) que hay que presionar y la URL donde encuentras esta información.
2. ¿Cuál es la última versión de BIOS/UEFI para la Asus M241?
3. Un propietario de una computadora Asus con Windows 10 quiere saber si este modelo se puede actualizar a Windows 11. Proporciona la URL donde encontraste esta información.
4. Un cliente posee una placa madre Tyan S7025. ¿Cuántas ranuras PCIe y de qué tipo tiene esta placa madre? Escribe la respuesta y la URL donde encuentras la respuesta.
5. En la misma placa madre Tyan S7025 de la pregunta 4, ¿qué puente de la placa madre se usa para limpiar el CMOS? Escribe la respuesta y la URL donde encuentras la información.
6. En la misma placa madre Tyan S7025 de la pregunta 4, ¿qué opción del menú del BIOS/UEFI se usa para configurar el orden en que el sistema busca dispositivos para arrancar la computadora? Escribe la respuesta y la URL donde encuentras la respuesta.

**Habilidades blandas**

Objetivo:
 Mejorar y afinar la capacidad de un futuro técnico para escuchar, comunicarse tanto de forma escrita como oral, y apoyar de manera profesional a las personas que usan computadoras

Actividades:

1. En equipos, planteen un escenario de solución de problemas que involucre a un técnico de computadoras que use técnicas de "pistolero" y el mismo escenario con un técnico que sea metódico. Expliquen qué hace cada tipo de técnico y cómo cada uno resuelve el problema. Además, detallen cómo estos dos técnicos tratan al cliente de forma diferente. Determinen las formas en que un técnico pistolero podría ser perjudicial para un negocio de reparación de computadoras. Demuestren o informen sobre sus hallazgos.
2. Después de explorar las opciones del BIOS/UEFI, dirígete a un compañero de clase, finge que él o ella es un cliente por teléfono y guía al estudiante a través del proceso de acceder a Setup. Explica los propósitos de al menos cinco de las opciones. Inviertan los roles y cubran otras cinco opciones. Asegúrate de actuar como un usuario típico de computadoras al desempeñar el papel de cliente.
3. Realiza una lluvia de ideas sobre un escenario de solución de problemas en el que arregles un problema que involucre acceder al programa Setup y/o a un adaptador. Documenta el problema usando una aplicación de procesamiento de textos. Crea una factura usando una aplicación de procesamiento de textos o de hojas de cálculo. Comparte tus documentos con otros en la clase.

**Habilidades de pensamiento crítico**

Objetivo:
 Analizar y evaluar información, así como aplicar la información aprendida a situaciones nuevas o diferentes

Actividades:

1. Describe una situación en la que creas que agregar una tarjeta eSATA tiene sentido.
2. Compara y contrasta una oficina de correos con las IRQ, las direcciones de E/S y las direcciones de memoria que se muestran en el Administrador de dispositivos. Por ejemplo, ¿cómo podría relacionarse algo que ocurre en una oficina de correos con una IRQ en una PC (o una dirección de E/S o de memoria)?
3. Tus padres tienen una computadora nueva, y ven un mensaje para presionar F2 para entrar a Setup. Lo hacen, y quieren que les expliques qué están viendo.
