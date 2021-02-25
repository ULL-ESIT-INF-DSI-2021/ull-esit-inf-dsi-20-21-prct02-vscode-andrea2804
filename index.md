# Práctica 2. Instalación y configuración de Visual Studio Code  
### Desarrollo de Sistemas Informáticos
### Andrea Hernández Martín - alu0101119137
[Enlace a la Github Page](https://ull-esit-inf-dsi-2021.github.io/ull-esit-inf-dsi-20-21-prct02-vscode-andrea2804/)

## Introducción
En esta práctica llevaremos a cabo la instalación y configuración del entorno de desarrollo Visual Studio Code. Además de la realización de un primer proyecto en TypeScript.  

## Instalación Visual Studio Code
Vamos a instalar VSCode en nuestra máquina local. Si estamos trabajando en una distribución Linux Debian/Ubuntu podemos instalarlo haciendo uso del siguiente comando:
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

A continuación en el VSCode, pulsamos sobre la tecla *F1* o la combinación de teclas *Ctrl + Shift + P* para mostrar la paleta de comandos, introducimos *ssh* y
pulsamos en *Remote-SSH: Connect to Host...*, ahí nos debería salir el nombre del host (en mi caso, iaas-dsi35) que habíamos configurado previamente en la práctica 1, pulsamos sobre el nombre y si todo ha ido bien, se conectará a nuestra máquina local. En caso de no haberlo configurado y no aparezca el nombre del host, entre a la [práctica 1](https://github.com/ULL-ESIT-INF-DSI-2021/ull-esit-inf-dsi-20-21-prct01-iaas-alu0101119137/blob/main/index.md) y realice el apartado 8.
En la siguiente imagen muestro lo que debería salir en la barra inferior del VSCode en caso de que esté conectado a la máquina virtual:  
![SSH en VSCode](https://raw.githubusercontent.com/ULL-ESIT-INF-DSI-2021/ull-esit-inf-dsi-20-21-prct02-vscode-andrea2804/main/img/Ssh_vsc.png?token=ALBLY3GP3A4T3O36GUEJH7DAID4AM)  

## Sesiones colaborativas con Visual Studio Live Share  
En este apartado vamos a configurar el modo Live Share de VSCode, ya que sirve para el trabajo colaborativo entre varias personas. Este modo
## Primer proyecto en TypeScript: “Hola Mundo”
## Conclusión
## Bibliografía
