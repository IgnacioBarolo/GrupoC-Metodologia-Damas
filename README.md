# GrupoC-Metodologia
PROYECTO DE METODOLOGÍA DE LA INVESTIGACIÓN

GRUPO C
-Barolo Ignacio
-Calderini Macarena
-Castillo Santiago
-Natel Guillermina

JUEGO:
“Mundamitas”

El proyecto se basa en un juego de damas, en el se podrá jugar multijugador en LAN con otra persona, esto se logra a través de Sockets.

Git: https://github.com/IgnacioBarolo/GrupoC-Metodologia-Damas

Instrucciones:
- Tener instalado Linux con la distribución que mas le guste.
- Instalar versión de Python 3.10.
- Instalar IDE Pycharm versión Community.
- Obtener las librerías necesarias(Pygame, Pip, etc).
- Crear carpeta, click derecho y abrir en la terminal
- Clonar Repositorio con los siguientes comandos:
	git clone https://github.com/IgnacioBarolo/GrupoC-Metodologia-Damas

![Imagen1](https://user-images.githubusercontent.com/103141746/233189616-5b17d44d-fc41-43ca-8971-b99b9a925844.png)


- Abrir Proyecto en Pycharm:
 
 ![Imagen2](https://user-images.githubusercontent.com/103141746/233189702-4fa8963e-7059-4593-b65e-004d96a6109a.png)

 
- Dirigirse a “File”, “Settings”, ir al nombre del proyecto, “Python Interprete” y seleccionar la ruta donde esta instalado Python 3.10:

![Imagen3](https://user-images.githubusercontent.com/103141746/233189774-135b8abe-3e7d-486a-84cb-4a6d9a48c127.png)


- Click derecho en la clase “server.py” y apretá “run”:

![Imagen4](https://user-images.githubusercontent.com/103141746/233189835-bd84d862-9d55-4d09-b53d-9319ba4ae6de.png)


- Click en edit configuración:

![Imagen5](https://user-images.githubusercontent.com/103141746/233189936-dc82c682-a524-40e9-ab51-1391dbd17793.png)


- Activar la opciòn “Allow parallel run”:

![Imagen6](https://user-images.githubusercontent.com/103141746/233189960-6841fe77-af56-4681-a4b0-968c7baadadb.png)


- Aplicamos los cambios(apply)


- Ejecutar la clase “menu.py”
Nota: Ejecutar dos veces menú para poder tener dos clientes y probar desde la misma maquina.
Si quiere probar el proyecto en dos computadoras, deberá cambiar la variable ADDR de la clase server y la variable ADDR de la clase Network. Una computadora sera el “Host”, entonces en el server deberá poner la IP de su computadora. La otra maquina solo deberá cambiar la IP de Network(se debe poner la IP del server)

- Se abrirá un menú en el cual le da “Play” y tendrá que esperar que se conecte el otro cliente para poder jugar:

![Imagen7](https://user-images.githubusercontent.com/103141746/233190020-b80e510a-c02c-4d1e-9718-187e24bbcecd.png)


- Disfrutar!!!

![Imagen8](https://user-images.githubusercontent.com/103141746/233190057-f7d9eb67-9cb8-41a1-adb9-849af0a52561.png)



LENGUAJE:
-Python

LIBRERÍAS:
- Pygame
- Socket

SISTEMA DE CONTROL DE VERSIONES:
- Git

IDE:
- Pycharm

VERSIONES:
- Python 3.10.4
- Git 2.36.0

PLANIFICACIÓN:
- Aprender reglas del juego de Damas.
- Análisis y relevamiento de las tecnologías a utilizar.
- Estudio del lenguaje, librería y sistema de versionado.
- Preparación y acondicionamiento del entorno de desarrollo (Descargas e instalación de programas/librerías requeridas).
- Diseño y Planificación de la lógica algorítmica.
- Diseñar boceto de la estructura y posibles funciones que se usarán.
- Codificación del programa por módulos(tablero, piezas, movimientos, reglas, main, menú,etc).
- Búsqueda exhaustiva de errores. Testing.
- Configuración del programa para uso en LAN.

DIVISIÓN DE TAREAS:
El proyecto se irá trabajando de manera conjunta para poder ayudarnos a resolver problemas que se vayan planteando.

HORAS ESTIMADAS DE PROGRAMACIÓN:
- 60-80 hrs.

CONEXIÓN LAN
Utilizaremos para la conexión el método sockets a través del puerto TCP/IP, creando dos módulos(cliente, servidor), en el cual se irá transfiriendo la información de los movimientos que se vayan realizando durante las partidas.

Un servidor levantara un socket, el cual es una combinación de dirección de red y puerto, bind agarra este socket y lo asocia con un recurso físico(tarjeta ethernet del equipo), es decir lo dispone hacia el exterior.

Listen coloca estas construcciones en modo escucha de modo que el servidor esté atento a conexiones entrantes.

Cliente levanta un socket y luego llama al método connect(el cual se bloquea), para intentar conectarse al servidor, cuando intenta establecer conexión, el método access y connect se desbloquean, una vez hecho esto se pueden hacer dos cosas,send y recv(enviar y recibir) desde el server al cliente o viceversa, el método recv estará bloqueado hasta recibir algo del otro extremo, utilizando send.

![Conexion LAN](https://user-images.githubusercontent.com/103141738/168706927-9343c5cb-7140-4ff1-ad66-c534d71eef89.png)
