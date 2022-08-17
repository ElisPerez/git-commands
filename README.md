# CONFIGURAR HERRAMIENTAS

- Configura la información del usuario para todos los respositorios locales

```
$ git config --global user.name "[name]"
// Establece el nombre que desea esté anexado a sus transacciones
de commit

$ git config --global user.email "[email address]"
// Establece el e-mail que desea esté anexado a sus transacciones de commit

$ git config --global color.ui auto
// Habilita la útil colorización del producto de la línea de comando
```

# CREAR REPOSITORIOS

- Inicia un nuevo repositorio u obtiene uno de una URL existente

```
$ git init [project-name]
// Crea un nuevo repositorio local con el nombre especificado

$ git clone [url]
// Descarga un proyecto y toda su historia de versión
```

# EFECTUAR CAMBIOS

- Revisa las ediciones y elabora una transacción de commit

```
$ git status
// Enumera todos los archivos nuevos o modificados que se deben confirmar

$ git add [file]
// Toma una instantánea del archivo para preparar la versión

$ git reset [file]
// Mueve el archivo del área de espera, pero preserva su contenido

$ git diff
// Muestra las diferencias de archivos que no se han enviado aún al
área de espera

$ git diff --staged
// Muestra las diferencias del archivo entre el área de espera y la última
versión del archivo

$ git commit -m "[descriptive message]"
// Registra las instantáneas del archivo permanentemente en
el historial de versión
```

# CAMBIOS GRUPALES

- Nombra una serie de commits y combina esfuerzos ya culminados

```
$ git branch
//Enumera todas las ramas en el repositorio actual

$ git branch [branch-name]
// Crea una nueva rama

$ git checkout [branch-name]
// Cambia a la rama especificada y actualiza el directorio activo

$ git checkout -b [branch-name]
// Crea una nueva rama y Cambia a la nueva rama especificada y actualiza el directorio activo

$ git merge [branch]
// Combina el historial de la rama especificada con la rama actual

$ git branch -d [branch-name]
// Borra la rama especificada
```

# NOMBRES DEL ARCHIVO DE REFACTORIZACIÓN

- Reubica y retira los archivos con versión

```
$ git rm --cached [file]
// Retira el ARCHIVO (FILE) del control de versiones, pero preserva el ARCHIVO (FILE) a
nivel local

$ git rm -r --cached build/
// Retira el DIRECTORIO (CARPETA) del control de versiones, pero preserva el DIRECTORIO (CARPETA) a nivel local

$ git rm [file]
// Borra el archivo del directorio activo y pone en el área de espera el
archivo borrado

$ git mv [file-original] [file-renamed]
// Cambia el nombre del archivo y lo prepara para commit
```

# SUPRIMIR TRACKING

- Excluye los archivos temporales y las rutas

```
$ git ls-files --other --ignored --exclude-standard
// Enumera todos los archivos ignorados en este proyecto
```

# GUARDAR FRAGMENTOS

- Almacena y restaura cambios incompletos

```
$ git stash
// Almacena temporalmente todos los archivos tracked modificados

$ git stash list
// Enumera todos los sets de cambios en guardado rápido

$ git stash pop
// Restaura los archivos guardados más recientemente

$ git stash drop
// Elimina el set de cambios en guardado rápido más reciente
```

# REPASAR HISTORIAL

- Navega e inspecciona la evolución de los archivos de proyecto

```
$ git log
// Enumera el historial de la versión para la rama actual

$ git log --follow [file]
// Enumera el historial de versión para el archivo, incluidos los cambios
de nombre

$ git diff [first-branch]...[second-branch]
// Muestra las diferencias de contenido entre dos ramas

$ git show [commit]
// Produce metadatos y cambios de contenido del commit especificado
```

# REHACER COMMITS

- Borra errores y elabora historial de reemplazo

```
$ git reset [commit]
// Deshace todos los commits después de [commit], preservando los
cambios localmente

$ git reset --hard [commit]
// Desecha todo el historial y regresa al commit especificado
```

# SINCRONIZAR CAMBIOS

- Registrar un marcador de repositorio e intercambiar historial de versión

```
$ git fetch [bookmark]
// Descarga todo el historial del marcador del repositorio

$ git merge [bookmark]/[branch]
// Combina la rama del marcador con la rama local actual

$ git push [alias] [branch]
// Carga todos los commits de la rama local al GitHub

$ git pull
// Descarga el historial del marcador e incorpora cambios
```

# COMANDOS EN LA TERMINAL

- A continuación vamos a explorar una serie de comandos básicos que podemos usar en nuestra terminal.

## Comandos básicos del sistema operativo

`date`: Muestra la fecha y hora del sistema actual.

`uptime`: Muestra el tiempo transcurrido desde que inició el equipo por última vez.

`cal`: Muestra un calendario del mes actual.

`df`: Muestra el espacio libre actual en el disco duro.

`whoami`: Muestra el nombre del usuario actual.

## Comandos para el manejo de carpetas

`ls`: Lista los archivos de la carpeta actual, o de la ruta dada. Ej. `ls Documents`.

`cd`: Nos permite navegar entre carpetas cuando le entregamos una ruta y así actualizar nuestra ubicación. Ej. `cd Documents` nos ubicaría en `/Users/<usuario>/Documents` y si hacemos ls veríamos el resultado del ejemplo anterior. Sin embargo, si hacemos uso de solo cd sin ruta, nos ubicaría en la carpeta de archivos del usuario.

`pwd`: Nos nuestra la ruta absoluta del directorio actual, así podemos saber en dónde estamos ubicados. Si estuviéramos ubicados como en el ejemplo anterior, esto nos devolvería el resultado `/Users/<usuario>/Documents`.

`mkdir`: Crea una nueva carpeta dado un nombre para esa carpeta. Ej. mkdir hola crearía una carpeta llamada hola en la ubicación en la que estemos.

`cp -r`: Nos permite copiar una carpeta dada una ruta inicial y una ruta final. La opción

`-r` significa que hará el proceso de manera recursiva, esto es porque al copiar una carpeta es necesario aplicar todos los archivos que están adentro. Ej. `cp -r hola alo`.

`rm -r`: Nos permite eliminar una carpeta dada una ruta. La opción -r significa que hará el proceso de manera recursiva, esto es porque al eliminar una carpeta es necesario aplicar todos los archivos que están adentro. Ej. `rm -r hola`.

## Comandos para el manejo de archivos

`touch`: Crea un archivo nuevo dada una ruta y/o nombre. Ej. touch chao crearía un archivo llamado "chao". Luego podríamos abrir este archivo con cualquier editor y agregar contenido. Sin embargo, podemos usar un pequeño truco para agregar contenido rápido haciendo echo 'hola mundo' > chao que remplazaría el contenido del archivo "chao" con "hola mundo".

`cat`: Imprime el contenido de un archivo dada su ruta. Ej. cat chao imprimiría hola mundo en nuestra terminal, en el caso de que hubiéramos seguido el ejemplo anterior.

`more`: Es muy similar a cat solo que nos permite navegar usando los controles tipo vim cuando imprime su contenido.

`cp`: Es el comando que nos permite copiar archivos dada una ruta inicial y una ruta final donde vamos a copiar. Ej. cp chao adios hará una copia del archivo "chao" y esta copia la llamará "adios".

`rm`: Nos permite eliminar un archivo dada una ruta. Ej. rm chao.

`mv`: Nos permite mover un archivo o carpeta dada una ruta inicial y una ruta final. Ej. mv adios /Users/<usuario>/Downloads movería la carpeta de la ubicación actual a la carpeta "Downloads". mv también es el comando que nos permite cambiar el nombre de un archivo o carpeta. Lo que hay que hacer es moverlo a la misma ubicación pero darle un nombre diferente, ej. mv adios bye.

## Rutas relativas y absolutas

- Las rutas se pueden especificar de manera relativa o absoluta. Cuando especificamos una ruta absoluta, quiere decir que vamos a introducir toda la ruta desde el inicio, es decir, desde la raíz, y esta se especifica con el símbolo de barra oblicua (slash) `/`. Cuando usamos el comando pwd siempre nos devuelve la ruta absoluta. Ej. `/Users/<usuario>`. Si estamos ubicados en nuestra carpeta de archivos y queremos movernos a la carpeta de documentos podemos especificar la ruta absoluta `/Users/<usuario>/Documents` o podemos especificar la ruta relativa a nuestra ruta actual `Documents`. Ahora bien, para poder especificar de manera relativa que queremos regresar un nivel, suponiendo que estamos en `Documents` y queremos regresar a `/Users/<usuario>` lo podemos hacer con el doble punto. Ej. `cd ../`. Así mismo, si queremos especificar la ubicación actual para movernos podemos usar solo un punto. Ej. `cd ./Documents`.

## Atajos de los comandos en la terminal

`Ctrl + c`: Muchas veces un comando puede quedarse procesando algo. Si queremos cancelar el comando actual o la terminal no responde podemos hacer uso de este atajo para detenerlo.

`Ctrl + u`: Nos permite borrar la línea actual que estemos escribiendo en la terminal.

`Ctrl + w`: Nos permite eliminar la última palabra de los comandos que estamos escribiendo en el momento.

`Ctrl + a`: Nos permite movernos al inicio de la línea de comandos.

`Ctrl + e`: Nos permite movernos al final de la línea de comandos.

`Flecha arriba`: Nos muestra el comando anterior de nuestro historial de comandos usados.

`Flecha abajo`: Nos muestra el comando siguiente de nuestro historial de comandos usados.

`Alt + b`: Nos permite movernos entre las palabras de la línea de comandos actuales hacia atrás.

`Alt + f`: Nos permite movernos entre las palabras de la línea de comandos actuales hacia adelante.

`Ctrl + r`: Nos permite hacer una búsqueda de comandos en el historial. Si encontramos un resultado que no es el deseado, podemos seguir presionando Ctrl + r para rotar la búsqueda.
