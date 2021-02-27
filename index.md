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

## Visual Studio Live Share  
En este apartado vamos a configurar el modo Live Share de VSCode, ya que sirve para el trabajo colaborativo entre varias personas. Este modo nos permite hacer proyectos en conjunto en tiempo real, además tiene un chat propio, se pueden hacer llamadas, compartir la terminal del proyecto y varias cosas más. Para más información sobre este modo colaborativo, podemos acceder a la página web de VSCode, [Collaborate with Live Share](https://code.visualstudio.com/learn/collaboration/live-share).  

Para configurarlo, lo único que tenemos que hacer es descargar la extensión *Live Share Extension Pack*, una vez instalada nos aparecerá el símbolo de una flecha con un punto en la barra lateral izquieda del VSCode. Ese es el símbolo de la extensión *Live Share*, por lo que cuando querramos utilizarla tendremos que pinchar en él.  

Para comenzar una sesión colaborativa tendremos que pulsar sobre *Share* y si es la primera vez que lo utilizamos nos pedirá iniciar sesión en Github o en Hotmail, elegimos la que queramos y seguimos los pasos que se nos muestran. Una vez iniciada la sesión, nos aparecerá al lado de la barra lateral izquierda un menú desplegable que pone *detalles de la sesión*, si queremos invitar a una o varias personas lo que tenemos que hacer es pinchar sobre *invite participants* dentro de ese menú y seguir los pasos que nos dice VSCode, también podemos hacer llamadas de audio haciendo click en *Start audio Call*. Una vez empezada la sesión colaborativa, podrás compartir con las personas que estén en el proyecto las terminales y los servidores, esto también se hará mediante el menú desplegable. Para saber más información de todas sus funcionalidades, acceder a la página web [Collaborate with Live Share](https://code.visualstudio.com/learn/collaboration/live-share).  
A continuación, adjunto algunas imágenes de cómo se vería el modo colaborativo en VSCode.  

## Introducción a TypeScript
En este apartamos vamos a realizar nuestro primer proyecto en Typescript, en primer lugar tenemos que instalar la extensión del VSCode *ESLint* que nos permite realizar comprobaciones de estilo sobre ficheros que incluyen código fuente en JavaScript y TypeScript, para instalarla hacemos como hicimos en los apartados anteriores buscando en el buscador de extensiones del VSCode.  

A continuación, vamos a instalar el compilador de TypeScript en nuestra máquina virtual. Para ello, abrimos una terminal en el propio VSCode, pulsando F1 y ejecutamos el comando siguiente:
```
[~()]$npm install --global typescript

changed 1 package, and audited 2 packages in 3s

found 0 vulnerabilities
```
Ahora que ya hemos instalado el compilador de Typescript, podemos empezar a crear nuestro primer proyecto. Vamos a crear un directorio llamado *hello-world* y accedemos a él, dentro de este ejecutaremos un comando que creará un fichero *package.json* que se utiliza para establecer las dependencias de desarrollo y ejecución del proyecto. Lo realizamos mediante los siguientes comandos:
```
[~()]$mkdir hello-world
[~()]$cd hello-world/
[~/hello-world()]$npm init --yes
Wrote to /home/usuario/hello-world/package.json:
{
  "name": "hello-world",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": ""
}

[~/hello-world()]$ls -lrtha
total 24K
drwxrwxr-x  4 usuario usuario 4,0K feb 23 19:24 .
drwxr-xr-x 11 usuario usuario 4,0K feb 24 10:49 ..
-rw-rw-r--  1 usuario usuario  225 feb 27 12:41 package.json
``` 
Con el último comando comprobamos el contenido de nuestro directorio *hello-world* y podemos observar que efectivamente se ha creado el fichero.  

Como ya tenemos el proyecto inicializado, ahora procedemos a abrir el proyecto en nuestro entorno de trabajo del VSCode . Para realizar esto, pulsamos sobre *File* y luego en *Open Folder*, seleccionamos el directorio que acabamos de crear (hello-world) y ya tendríamos abierto nuestro proyecto, lo que nos permitirá visualizar el contenido de este.  

Una vez abierto el proyecto, vamos a crear un fichero llamado *tsconfig.json* dentro de nuestro directorio *hello-world* en el que de especificarán las opciones del compilador de TypeScript. 
```
[~/hello-world()]$touch tsconfig.json 
[~/hello-world()]$cat tsconfig.json 
{
  "compilerOptions": {
    "target": "ES2018",
    "outDir": "./dist",
    "rootDir": "./src",
    "module": "CommonJS"
  }
}
```
Los datos introducidos anteriormente en el fichero significan que mediante *"target"* queremos generar código compatible con uno de los últimos estándares de JavaScript, con *"outDir"* indicamos que el código JavaScript se almacenará en un directorio *dist*, *"rootDir"* indica que el código fuente escrito en TypeScript se va a encontrar en el directorio *src* y por último con *"module"* especificaremos un estándar para cargar código desde ficheros independientes.  

A continuación, vamos a crear un fichero con código TypeScript dentro de un directorio que crearemos y llamaremos *src*, una vez creado, accedemos a ese directorio y creamos el fichero TypeScript llamado *index.ts*. Ahora, dentro del fichero añadimos el código necesario para hacer un *Hello World*. Todo esto lo haremos ejecutando los siguientes comandos:
```
[~/hello-world()]$mkdir src
[~/hello-world()]$cd src/
[~/hello-world/src()]$touch index.ts
[~/hello-world/src()]$vim index.ts 
  let myString: string = "Hola Mundo";
  console.log(myString);
```
Para compilar el código anterior, solo tenemos que escribir el siguiente comando en la terminal de VSCode:
```
[~/hello-world/src()]$tsc
```

Una vez ejecutado el comando anterior, habrá creado el directorio *dist* y el fichero *index.js* automáticamente. Los podemos comprobar para ver si hay alguna diferencia entre el creado autómaticamente (.js) y el creado por nosotros anteriormente (.ts) de la siguiente forma:
```
[~/hello-world()]$diff src/index.ts dist/index.js
1c1
< let myString: string = "Hola Mundo";
---
> let myString = "Hola Mundo";
```

Que cómo podemos observar, los códigos son casi iguales exceptuando la declaración de la variable *myString*.  

Para finalizar el proyecto, ejecutaremos el código JavaScript generado a partir del código TypeScript:
```
[~/hello-world()]$node dist/index.js
Hola Mundo
```

## Conclusión
## Bibliografía
