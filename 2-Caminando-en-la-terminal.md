En los sistemas operativos organizamos los archivos en una estructura de carpetas en forma de árbol jerárquico. Este árbol cambia dependiendo de los diferentes sistemas operativos (no tanto en Linux y Mac).

**Cómo funciona el sistema de carpetas**
El sistema operativo con el que trabajaremos es Linux, por lo tanto usaremos su estructura.

La carpeta con el símbolo “/” es la raíz, ahí es donde comienza todo el sistema de ficheros (el equivalente en Windows podría ser el fichero “C:\”). Dentro de esta carpeta hay varios ficheros, el que nos importa en este momento es el “Home”.

La carpeta “Home” contiene una carpeta por cada usuario del sistema y ya dentro de cada una de estas carpetas, estarán las carpetas que conocemos de toda la vida como imágenes, documentos, música, etc.

Cómo entender la información al inicio de la terminal
Cuando abrimos la terminal vamos a ver algo como esto:

lorecg@DESKTOP-3R804MK:~$

Todo esto parece un mensaje encriptado, pero es más sencillo de lo que parece, vamos por partes:

- lorecg es el nombre del usuario que está activo. En tu caso aparecerá el nombre del usuario que esté activo en tu computadora.

- DESKTOP-3R804MK es el nombre que el sistema operativo le dio a la computadora. En este caso se usa Windows y ese es el nombre que en la instalación Windows le asignó al dispositivo. Si usas Linux aparecerá el nombre del PC que hayas colocado en la instalación.

- ~ es la carpeta en la que te encuentras y ahora es cuando empiezan las confusiones porque en el esquema no estaba una carpeta con ese símbolo. Más adelante verás como todo tiene sentido.

- Por último, $ significa que somos un usuario normal y no un root o un superusuario. Más adelante hablaremos más acerca de esto.

**Tu primer comando** (pwd)
Ahora sí, vamos con el poderosísimo comando que te ayudará a descubrir algo muy importante: ¿dónde estás?

Vimos que el símbolo ~ indica la carpeta donde te encuentras, ¿cuál es esa carpeta? Para saberlo escribe el siguiente comando:

*pwd*

debió haber aparecido algo como esto:

/home/lorecg

El comando pwd, significa Print Working Directory y muestra el directorio en el que te encuentras.

Usar el comando Change Directory (*cd*)
No trabajarás todo desde la misma carpeta, así que necesitas saber como moverte entre carpetas sin salir de la terminal. Para eso usamos el comando cd que significa Change Directory.

Para usarlo escribimos cd seguido del directorio al que queremos movernos, por ejemplo, dentro del home tengo la carpeta Documents, así que para moverme ahí escribo:

cd Documents

Y ahora vemos que la información que nos muestra la consola cambió y nos indica donde estamos:

lorecg@DESKTOP-3R804MK:~/Documents$

**Atajos**

- Virgulilla (~) alt+126

De seguro te preguntarás porqué la virgulilla (~) indica la carpeta del usuario en el home, ¿cuál es la utilidad? Supongamos que estamos navegando por diferentes carpetas y nos encontramos en la siguiente dirección:

lorecg@DESKTOP-3R804MK:/mnt/c/users/lore/development$

(Si estás usando WSL, eso significa que estás buscando entre carpetas que están en Windows)

Si ahora quieres volver al home habría que escribir el siguiente comando:

cd /home/lore

Pero puedes mejor escribir:

cd ~

Y llegas más rápido.

- Punto y doble punto (.) (…)

No siempre quieres ir hacia adelante, a veces necesitas devolverte, para eso utilizas el atajo del doble punto (…) que te envía a la carpeta que está atrás. Si haces esto:

lorecg@DESKTOP-3R804MK:~$ cd ..

Como estás en la carpeta del usuario, pasarás a estar en la carpeta de home.

Por otro lado, el punto (.) índica la carpeta actual, así puedes hacer direcciones más precisas como esta:

lorecg@DESKTOP-3R804MK:/home$ cd ./lore/Documents/

- Slash (/)

Por último, el atajo slash te lleva a la raíz donde están todas las carpetas del sistema operativo.

lorecg@DESKTOP-3R804MK:/mnt/c/users/lore$ cd /
lorecg@DESKTOP-3R804MK:/$

***¿Cómo saber lo que hay adentro de las carpetas? (ls) ***

No siempre vas a saber lo que hay adentro de las carpetas, por lo que necesitas listar lo que hay dentro, para eso está el comando ls, por lo general le dan el significado de List.

- Si ejecutamos el comando *ls* veremos las carpetas y archivos que hay dentro.

Cada nombre tiene un color diferente. Para este caso el azul oscuro es para las carpetas y el claro es para los archivos, esto dependerá de la paleta de colores que tenga tu terminal.

Pero, ¿qué tal si queremos conocer más información? Para saber información adicional como la fecha de creación, el peso, los permisos, etc., utilizamos la opción -l que significa Long.

- Uso del comando *file*

Con el comando ls podemos listar los elementos dentro de una carpeta, pero a veces no sabemos si es una archivo o si es una carpeta o lo que sea.

Para eso tenemos el comando file que te da información acerca del tipo de elemento que hayas seleccionado.

-----------------------------------------------------------------
Comando:
pwd - Print Working Directory Muestra en la carpeta en la que estas
cd - Change Directory Te mueve a la carpeta que desees
ls - List Lista los archivos y carpetas dentro del directorio que selecciones
file -  Muestra la información del archivo que selecciones
-----------------------------------------------------------------

**Lecturas recomendadas**

[Linux File Hierarchy Structure - GeeksforGeeks](https://www.geeksforgeeks.org/linux-file-hierarchy-structure/)
