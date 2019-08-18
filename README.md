# Curso-Prework-Buenas-Practicas-y-Entorno-de-Desarrollo
Curso Platzi
# TABLA DE CONTENIDO
- [Terminal](#Terminal) 
- [Crea llaves SSH](#Crea-llaves-SSH) 
- [Configuración de la terminal MacOS](#Configuración-de-la-terminal-MacOS)
- [Instalación y configuración de VSCode](#Instalación-y-configuración-de-VSCode)
- [cómo instalar NodeJS](#cómo-instalar-NodeJS) 
- [Cómo ejecutar Node](#Cómo-ejecutar-Node)
- [](#)
- [](#) 
- [](#) 
- [](#)
- [](#)
- [](#) 
- [](#)
- [](#)
- [](#) 
- [](#) 
- [](#)
- [](#)
- [](#) 
- [](#)
- [](#)
<!-- toc -->
## Terminal
**Manejo archivos y directorios**
Vamos a ver diferentes comandos que nos serán de gran utilidad:

ls: Nos permite listar los archivos y directorios que se encuentren dentro de la carpeta en la que estamos ubicados, podemos pasarle distintos parámetros a este comando:
-a podemos ver los archivos ocultos.
-l nos lista los contenidos mostrando  sus permisos y propietarios.
-t nos lista los contenidos según su fecha.
clear: Nos limpia la pantalla. contr l
pwd: Nos retorna la ruta absoluta en la cual nos encontramos.
mkdir: Crea una carpeta.
cd: Nos mueve a alguna carpeta que le indiquemos, dentro de los archivos ocultos vimos que existe:
.: Refiere a la carpeta en la cual estamos ubicados.
..: Se refiere a la carpeta padre en la cual nos encontramos.
history: Muestra el histórico de todos los comandos que hemos ejecutado.
touch: Crea un archivo vacío con el nombre que le indiquemos.
nano: Es un editor dentro de la consola, podemos abrir cualquier archivo y modificarlo.
mv: Permite mover archivos entre distintas carpetas, solamente debemos indicarle el nombre del archivo y la ruta de destino.
rm: Elimina únicamente un archivo, añadiendo el parámetro -rf podemos eliminar directorios también.

**Herramientas básicas (Comandos CAT, MORE, TAIL y OPEN)**
cat: permite visualizar un archivo completo en la terminal.
more: muestra por partes un archivo dentro de la terminal.
tail: muestra las últimas 10 líneas de cada archivo, se puede modificar pasándole el parámetro con el número de líneas -15.
open: abre un archivo con el programa que tengamos por defecto.

➜  buenasPracticasDev git:(master) cat README.MD > copy_README.md

## Crea llaves SSH
Las llaves SSH nos van a ayudar para autentificarnos con servidores. SSH utiliza criptografía asimétrica, o sea, tenemos dos llaves:

Pública: la llave pública la podemos compartir por internet.
Privada: debes tenerla en un sitio seguro y no debe ser compartida.
Tener una llave SSH nos permitirá una conexión fácil y segura con servidores, en el caso de la escuela de JavaScript nos va a servir para conectarnos con GitHub.

Para crear una llave SSH utilizamos el siguiente comando:
```
ssh-keygen -t rsa -b 4096 -C  
``` 
~ ssh-keygen -t rsa -b 4096 -C "This is a key"

## Configuración de la terminal MacOS

https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH
https://hyper.is/
https://ohmyz.sh/
https://github.com/robbyrussell/oh-my-zsh/wiki/Themes

## Configuración de ZSH para windows con linux shell
- settings - update & security - developer mode - 
https://docs.microsoft.com/en-us/windows/wsl/install-win10

- luego que se instala ubuntu como lo indica lapágina
sudo apt-get install zsh
- luego se instala Oh-myzsh
- chsh -s /user/bin/zsh
- hyperp editar y en shell:'C:\\WINDOWS\\System32\\bash.exe'

## Instalación y configuración de VSCode
Si la primera mejor amiga del programador es la línea de comandos, es momento de instalar y configurar el segundo mejor amigo del programador: el editor de código.

Existen multiples editores de código, para la escuela de JavaScript vamos a utilizar Visual Studio Code. Vamos a añadir diferentes plugins para VSCode:

Git Blame: va a mostrar el autor de la línea de código en la que estemos trabajando.
ESLint: es una herramienta de análisis de código estático para identificar patrones problemáticos encontrados en el código JavaScript, o sea, nuestro linter. Debemos instalar y configurar eslint para que siga el estilo de código que le indiquemos.
Color Highlight: resalta el color que estemos escribiendo.
SASS: es un preprocesador de CSS.

npm install -g eslint
npx eslint --init
➜  buenasPracticasDev git:(master) npx eslint --init
? How would you like to use ESLint? To check syntax, find problems, and enforce
code style
? What type of modules does your project use? JavaScript modules (import/export)


? Which framework does your project use? React
? Where does your code run? (Press <space> to select, <a> to toggle all, <i> to
invert selection)Browser
? How would you like to define a style for your project? Use a popular style gui
de
? Which style guide do you want to follow? Airbnb (https://github.com/airbnb/jav
ascript)
? What format do you want your config file to be in? JSON
Checking peerDependencies of eslint-config-airbnb@latest
? The style guide "airbnb" requires eslint@^5.16.0 || ^6.1.0. You are currently
using eslint@6.0.1.
  Do you want to downgrade? Yes
The config that you've selected requires the following dependencies:

eslint-plugin-react@^7.14.3 eslint-config-airbnb@latest eslint@^5.16.0 || ^6.1.0 eslint-plugin-import@^2.18.2 eslint-plugin-jsx-a11y@^6.2.3 eslint-plugin-react-hooks@^1.7.0

## Cómo instalar NodeJS


Node es el entorno de ejecución que tenemos para JavaScript en el lado del servidor, está basado en el motor V8 de Google Chrome. Fue creado por Ryan Dahl en el 2009, es Open Source y multiplataforma. En esta clase vamos a aprender cómo instalarlo, cómo usarlo y cómo instalar paquetes usando npm.

Revisión de Node en nuestro sistema
En la mayoría de sistemas basados en Unix ya viene instalado por defecto Node, para asegurarnos de que esté instalado debemos irnos a nuestra terminal de comandos y ejecutar:
$ node -v

Esto nos debería mostrar la versión de node que tenemos instalados en el sistema, por ejemplo:
$ node -v v12.4.0

Si la respuesta que obtenemos es:
$ node -v command not found: node

Debemos instalarlo

Instalación de Node en MacOS
Para esta instalación vamos a requerir de homebrew. Este es un gestor de paquetes excelente para Mac y que vamos a usar en varias clases de este curso, si no lo tienes instalado lo mejor es que lo hagas. En este link https://brew.sh/index_es encontrarás los pasos necesarios para instalarlo.
Una vez tengamos instalado homebrew solo debemos ejecutar en la terminal
$ brew install node

Este proceso podría tardar un rato dependiendo de la velocidad a la conexión a internet, ya que cuando se intenta instalar un paquete con homebrew este intenta actualizar todos los paquetes que se han instalado con él. Una vez esté listo puedes escribir en la terminal:
$ node -v

y ya debería aparecerte la versión instalada que tienes de Node. Igualmente, con npm ejecutaremos:
$ npm -v

y debería salirte la versión que tienes de npm.

Instalación de Node en Linux
Dependiendo de tu distribución de Linux deberás ejecutar comandos distintos, esto porque entre distribuciones cambiar el gestor de paquetes:
En distribuciones basadas en Debian y Ubuntu debes ejecutar:

$ sudo apt update

$ sudo apt install nodejs

$ sudo apt install npm

En distribuciones basadas en Arch:

$ pacman -S nodejs npm

Instalación de Node en Windows:
Esta es la instalación más sencilla y es una instalación clásica en Windows, únicamente descargamos un programa y le damos continuar, o si prefieres configuras la instalación según las opciones que están disponibles. El programa se descarga desde acá https://nodejs.org/en/#download y seleccionas la versión que desees (recomendada la versión igual o superior a las 12)

## Cómo ejecutar Node
Una vez se tenga instalado Node en el sistema podemos hacer uso de él, en esta clase haremos un uso básico de sus comandos, a lo largo de la Escuela de JavaScript será utilizado. Lo primero que haremos será ejecutarlo y escribir un Hola mundo. En la terminal haremos lo siguiente:
$ node
> console.log('Hola mundo')
Hola mundo
>

Al escribir node se nos abrirá un shell interactivo donde podremos escribir código en JavaScript. Esta herramienta es esencial en el desarrollo porque es aquí donde podremos probar funcionalidades antes de insertarlas en nuestro proyecto.

Cómo utilizar npm
npm es el manejador de paquetes de Node con él podemos instalar dependencias a nuestro proyecto o instalar programas globalmente en nuestro sistema. A lo largo de este curso y de toda la Escuela de JavaScript npm será quien nos permita correr los proyectos e instalar nuestras dependencias.
