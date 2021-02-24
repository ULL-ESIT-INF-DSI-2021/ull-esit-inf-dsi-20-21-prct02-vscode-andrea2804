# Práctica 2. Instalación y configuración de Visual Studio Code  
### Desarrollo de Sistemas Informáticos
### Andrea Hernández Martín - alu0101119137
[Enlace a la Github Page](https://ull-esit-inf-dsi-2021.github.io/ull-esit-inf-dsi-20-21-prct02-vscode-andrea2804/)

## Introducción
En esta práctica llevaremos a cabo la instalación y configuración del entorno de desarrollo Visual Studio Code. Además de la realización de un primer proyecto en TypeScript.  

## Instalación y funcionalidad de Visual Studio Code
Visual Studio Code (VSCode) es uno de los entornos más utilizados por los desarrolladores. Como primer paso, vamos a instalar VSCode en nuestra máquina local. Si está trabajando en una distribución Linux Debian/Ubuntu puede instalarlo haciendo uso del siguiente comando:
```
andrea@andrea-laptop:~$ sudo apt install code
```  
En caso de estar trabajando en una máquina MacOS o Windows, accedemos a la página de [instalación de VSCode](https://code.visualstudio.com/) y descargamos la que nos corresponda y se instalará automáticamente.  

## Configuración de Visual Studio Code para conectarse a una máquina remota por SSH
A continuación, vamos a explicar cómo tenemos que hacer para conectarnos a una máquina mediante SSH. Para ello, en primer luegar debemos estar conectados a la red VPN de la ULL y en segundo lugar, probar a conectarnos desde una terminal a nuestra máquina virtual mediante SSH con el siguiente comando:
```
andrea@andrea-laptop:~$ ssh iaas-dsi35
```
Una vez comprobado que hemos podido realizar la conexión, abrimos el VSCode e instalamos la extensión *Remote-SSH*.  
En caso de no saber instalar una extensión realizamos los siguientes pasos: dentro del VSCode vamos a la barra lateral izquierda y buscamos un símbolo con cuatro cuadrados pequeños juntos, pinchamos ahí y nos sale un buscador en el que pondremos el nombre de la extensión que queremos y nos aparecerá el nombre de la extensión y un pequeño botón de instalar, lo pulsamos y ya tendríaos la extensión instalada. En algunos casos, sale una ventana emergente del VSCode de que tiene que reiniciarse para poder utilizar esa extensión, le damos a reiniciar y ya tendríamos la extensión que queremos. En caso de querer más información vamos a la página web de VSCode que lo explica, [Extension Marketplace](https://code.visualstudio.com/docs/editor/extension-gallery).

## Sesiones colaborativas con Visual Studio Live Share
## Primer proyecto en TypeScript: “Hola Mundo”
## Conclusión
## Bibliografía
