---
title: "Eliminar carpeta node_modules o cualquier otra que hallamos agregado a git y queramos removerla"
date: 2022-04-24
description: 'Ha iniciado más a fondo el curso de Node.js y con el, algunos errores sobre la marcha, sí, subí a git la capeta node_modules. Si como a mi te ha pasado, en este artículo te platico cómo hice para borrar la carpeta de git.'
---

Hola lector, gracias por estar aquí nuevamente.

Hace unas semanas iniciamos en el curso de LaunchX a conocer más sobre Node.js, iniciamos con lo básico que es la inicialización del proyecto mediante el comando npm init, después instalamos Jest, un framework para pruebas. Cuando por primera vez instalamos un paquete, estó creará la carpeta node_modules dentro de nuestro proyecto, la cual contiene, todos los paquetes, ficheros y dependencias necesarios para el proyecto. Si versionas tus proyectos, y no tienes cuidado como yo, esta carpeta se subirá a tu repositorio y tardará un buen rato, pero no te preocupes, si ya la subiste y quieres eliminarla a continuación te cuento cómo eliminarla.

Para ello, sólo debes ejecutar los siguientes comandos:

```
1. git rm --cached node_modules
```

Lo que hace este comando es pedirle a git que remueva los archivos indicados sólamente del repositorio de git pero no de nuestro sistema o repositorio local. Si el directorio o archivo que necesitas remover es otro, en lugar de poner node_modules, indica la ruta de tu directorio o archivo.

```
2. Crear archivo .gitignore y agregar la carpeta node_modules de la siguiente manera: **/node_modules
```

El archivo .gitignore es un archivo de texto que le dice a Git qué archivos o carpetas ignorar en un proyecto

```
3. git commit -m 'Added node_modules to .gitignore file. Also removed node_modules from git tracking and repository.'
```

Agregar commit de los cambios que hicimos.

```
4. git push origin master'
```

Si el repositorio local está conectado a un repositorio remoto, subimos los cambios mediante el comando push.

Si buscas en Internet, encontrarás muchos artículos sobre como hacerlo, mi recomendación es tener cuidado con los comandos que ejecutas, yo sin querer, ejecuté el siguiente:

```
git rm -r --cached .
```

Como verás, al final en lugar de indicar una carpeta o archivo específico, estoy indicando con un punto que remueva todos los archivos, al hacerlo entré en pánico al ver que estaba agregando todos los archivos de mi proyecto para ser removidos, pero no hay nada que no tenga solución, si sin querer te pasa como a mi, solamente debes ejecutar el siguiente comando:

git reset .

Lo que hará este último comando es deshacer el cambio, una vez que los cambios se deshicieron, ejecuta los puntos del 1 al 4.

Ahora ya puedes remover archivos que requieras para que no estén dentro de un repositorio.

Gracias por leerme y mucha buena vibra para todos :D.

![Buenas vibras](https://media0.giphy.com/media/qVMWAFTTfINq/giphy.gif?cid=790b7611b66a60e81d5293d40006cd33ce01c37aa8e76de4&rid=giphy.gif&ct=g)