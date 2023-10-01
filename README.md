# LuisValencia-mi-proyecto-npm

Esta es la solución a la primera tarea asignada al equipo Frontend para mejorar las habilidades en esta área. La solución pertenece al tema: "Acerca de NPM, lo que no sabes a pesar que lo usas más que el jabón".

## Table of contents

- [¿Cómo crear un proyecto con NPM?](#Como)
- [¿Qué son los paquetes o módulos en NPM?](#Como)
- [¿Qué son las dependencias y cómo gestionarlas?](#Como)
- [¿Qué son y cuál es la diferencia entre CommonJS y ESModule?](#Como)
- [¿Qué es GIT, cómo funciona el rastreo de archivos y cómo ignorar archivos?](#Como)


## ¿Cómo crear un proyecto con NPM?
Como parte del entorno de ejecución de Javascript llamado Node.js, **NPM (Node Package Manager)**, corresponde a una parte importante que se encarga de la gestión de paquetes.
###
Podemos interpretar al NPM como al menos dos partes principales:
###
Por un lado, es un **repositorio en línea** donde podemos publicar paquetes de software libre para ser usados en proyectos de Node.js.
###
Por otro lado, es una **herramienta en la línea de comandos** que nos permite acceder, manejar o publicar paquetes dentro del repositorio.
## ¿Qué son los paquetes o módulos en NPM?
Los paquetes son, como su nombre lo describe, bloques. En este caso, bloques de código que contienen funciones, bibliotecas, frameworks... Cualquier código que sea de utilidad para una aplicación. Se utiliza NPM para instalar de manera sencilla estos bloques de código y evitarnos tener que realizarlo por nuestra cuenta.
## ¿Qué son las dependencias y cómo gestionarlas?
Cuando hacemos uso de una serie de paquetes que se encuentran disponibles en NPM y son constantemente mantenidos por otras personas, estamos haciendo uso de Dependencias.
###
Estos son paquetes externos que agregamos a nuestro proyecto para que funcione correctamente. Para poder agregar dependencias, nuestro proyecto Javascript debe ser un proyecto generado con NPM.
###
Generar el proyecto con NPM nos permite hacerle saber al gestor que manejaremos paquetes en nuesto proyecto. Para que esto funcione, el gestor crea en nuestro proyecto un archivo llamado **package.json**, que contiene la configuracion del proyecto en cuando a paquetes. Contiene sus nombres y sus versiones.
###
Aquí tenemos una lista de comandos y su explicación para la gestión de dependencias:
###
- `npm init`
    + Este comando se utiliza para **inicializar** un proyecto con NPM, luego de una serie de preguntas que podemos llenar por defecto presionando enter en cada una, se crearé nuestro proyecto incluyendo un archivo package.json en él.
- `npm install`
    + Este comando **instalará** o actualizará todas las dependencias en nuestro proyecto, siempre y cuando estén declaradas dentro del archivo package.json
- `npm install nombre-paquete`
    + Este comando se utiliza para **agregar** un paquete en específico a nuestro proyecto. De no especificar la versión, se añadirá la versión más reciente en el repositorio de NPM.
- `npm uninstall nombre-paquete`
    + Este comando se utiliza para **eliminar** un paquete en específico de nuestro proyecto. No es necesario especificar versiones.
## ¿Qué son y cuál es la diferencia entre CommonJS y ESModule?
**CommonJS** es una especificación (reglas o estándar), para la carga de móduls en javascript. Suele usarse en entornos de servidor por su carga sincrónica. Es característico porque carga primero todo el contenido del módulo, antes de ser ejecutado el fragmento de código donde es requerido.
###
**ESModule** es un sistema de módulos para javascript (también una especie de estándar), incorporado en especificaciones mpas recientes. Significan una forma más facil de exportar e importar módulos. Su característica principal es que tiene carga asincrónica, lo cual mejora el rendimiento de las aplicaciones.
###
Las diferencias notables entre ambas especificaciones son, su carga y su sintaxis, es mucho más facil de interpretar la sintaxis de un ESModule que de un módulo CommonJS.
## ¿Qué es GIT, cómo funciona el rastreo de archivos y cómo ignorar archivos?
La herramienta GIT es un software que maneja repositorios locales para el control de versiones de nuestros proyectos. Esta herramienta nos permite cambiar entre distintas versiones de nuestro proyecto ahorrándonos la necesidad de crear un complejo sistema de archivos.
###
Suele usarse de manera complementaria con GITHub que es un sistema de alojamiento de repositorios en la nube.
###
El rastreo de archivos se ejecuta de la manera siguiente:
###
- `git init`
    - Este comando **inicializa** un repositorio en nuestro equipo, aquí se registran los archivos que indiquemos a GIT que es necesario que tengan seguimiento.
- `git add`
    - Este comando **agrega** un archivo al área que llamamos "stage". Esta es un área de preparación a donde agregas los archivos en los cuales has hecho modificaciones y que se incluirán en el proximo commit. Como parámetro recibe el nombre del archivo a agregar (`git add nombre_archivo`), o un punto en su lugar para indicar que realice seguimiento a todos los archivos contenidos en la carpeta actual (`git add .`).
- `git commit -m "Descripción de los cambios"`
    - Este comando **actualiza** los archivos que indicamos con el comando anterior, enviando esos cambios al repositorio local que ha creado GIT. Se puede tener información adicional de este commit y del repositorio en general utilizando otros comandos. Estos son los básicos para la gestión de un repositorio local.
###
También, existe la posibilidad de ignorar permanentemente archivos al momento de crear nuestro repositorio local. Esto permite controlar qué archivos o carpetas no serán rastreados en ningún momento, útil para controlar archivos que manejan información sensible o información que se actualiza constantemende desde repositorios en linea (cómo dependencias de NPM). Esto se logra mediante el archivo **.gitignore**
###
La sintaxis de este archivo es bastante sencilla, acá se muestra un ejemplo sencillo del contenido de un archivo .gitignore
###
```
# Archivos que se excluyen del seguimiento en este repositorio
# También se excluye la carpeta de módulos de node
prueba.js
lista-usuarios.html
/node_modules
```