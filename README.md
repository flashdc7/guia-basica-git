# Git

## Instalacion Git
>1. https://git-scm.com/
>2. Una vez instalado corremos el siguiente comando `git --version`



## Instalaciones Plugins
>1. [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)



## Ayuda de Git
>- `git --help`
>- Ej. `git --help commit` o `git --help config`
>- Para salir de la ayuda solo presionamos la letra Q



## Configuración de Git localmente

> Cambiar nombre de la rama principal al inicializar un proyecto de master al nombre main
>- `git config --global init.defaultBranch main` 

> Nombre de usuario:
>- `git config --global user.name "FlashDC8"` 

>Email del usuario:
>- `git config --global user.email "ejemplo@mail.com"`

> Listamos nuestras configuraciones locales:
>- `git config --global -e`

> Para salir del modo de edición:
>- Presionamos `ESC`, después escribimos `:q!` y presionamos `ENTER` si no queremos guardar ningún cambio
>- Presionamos `ESC`, después escribimos `:wq!` y presionamos `ENTER` para guardar cambios y salir



## Inicializamos Git
>- Abrimos consola y escribimos `cd` y presionamos la tecla de espacio
>- Arrastramos la carpeta de nuestro desarrollo a la terminal para ubicarnos dentro de ella y presionamos `ENTER`
>- Inicializamos git con el siguiente comando `git init` y presionamos `ENTER`
>- Escribimos el comando `git status` y presionamos `ENTER` para ver la rama en la que nos encontramos, los commits y finalmente los archivos traqueados y no traqueados
>- Podemos agregar los archivos a nuestro commit de dos formas
>   - Uno por uno `git add mi_archivo.html`
>   - Todos los arhivos en un solo paso `git add .`
>- Para remover un archivo que no deseamos traquear
>   - Escribimos el comando `git reset nombre_del_archivo.html`y presionamos enter y con esto este archivo ya no es parte del stage antes del commit
>- Realizamos nuestro commit con el comando `git commit -m "nombred_del_commit"` y presionamos enter
>- Listamos nuestro(s) commit(s) con el siguiente comando `git log` 
><br ><br >![git init](images/git-init.png)<br >
>- Una forma abreviada de hacer commit es `git commit -am "nombre_del_commit"`, con esta opción solo se guardan en el commit los archivos a los cuales se les esta dando seguimiento y deja fuera los nuevos archivos



>## Restaurar un proyecto a como estaba al último commit
>- `git checkout -- .`



>## Ramas en Git
>- Para saber en que rama nos encontramos actualmente escribimos el comando `git branch` y presionamos enter
>- Es recomendable trabajar en diferentes ramas todas y solo la principal usarla para los cambios que se van a producción
>- Renombrar una rama. Ej del nombre ***master*** a ***main***, escribimos el comando `git branch -m master main` y presionamos enter

 

 >## Agregar archivos de un solo tipo o directorio
 >- Archivos html en raíz `git add *.html`
 >- Agrega los archivos js de la carpeta `git add js/*.js`
 >- Toma todos los archivos y directorios que se encuentra en este path `git add css/`



 >## ****** Seguimiento a carpetas ******
 >- ** Git no da seguimiento a carpetas que se encuentran totalmente vacias
 >- Para mantener un directorio vacio en nuestro repositorio que sabemos que necesitamos en nuestro proyecto solo agregamos dentro del directorio el siguiente archivo **.gitkeep**
><br ><br >![gitkeep](images/gitkeep.png)<br >
><br >![gitkeep](images/gitkeep-2.png)<br >


>## Creación de ALIAS para nuestros comandos
>- Son versiones cortas de los comandos de git, para crear un alias escribimos el siguiente comando `git config --global alias.nombre_del_alias seguido de los comandos que deseamos agregar entre comillas`
>- Ej `git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"` 
>- Para modificar un alias tecleamos el siguiente código `git config --global -e`
><br><br>![git alias](images/alias.png) <br><br>
>- Una vez que terminamos la edición presionamos ESC después :wq!
>- Y a continuación corremos nuestro alias y se vería de la siguiente forma
><br><br>![git alias](images/alias-lg.png) <br><br>



>## Ver las modificaciones 
>- Para ver los ajustes que realizamos antes de añadirlos al stage insertamos el siguiente código en consola `git diff` y presionamos ENTER
>- Para ver los ajustes que realizamos después de añadirlos al stage insertamos el siguiente código en consola `git diff --staged` y presionamos ENTER



>## Actualizar mensaje del commit y revertir commit
>- Para actualizar el nombre del último commit ingresamos el siguiente código `git commit --amend -m "nuevo_nombre_del_commit"` y presionamos ENTER
>- Si queremos ingresar a modo edición desde terminal entonces escribimos `git commit --amend` y presionamos ENTER
>- Una vez que ingresamos presionamos la tecla A y nos movemos con las flechas direccionales. Ya terminada la edición presionamos ESC después escribimos `:wq!`
><br><br>![git amend](images/amend-consola.png)<br><br>
>- Para revertir un commit ingresamos el siguiente comando `git reset --soft HEAD^` y presionamos ENTER. Con esto lo que hacemos es eliminar el último commit sin perder los cambios que se habian realizado en los archivos
>- Igual podemos cambiar por el HEAD por el hash de commit que deseamos revertir `git reset --soft 527f33b` o colocando el numero de commits antes del último `git reset --soft HEAD^2` 
>- Cuando hacemos el reset a un punto de la historia perdemos de vista todos los commits posteriores, para visualizar nuevamente estos commits ingresamos `git reflog` y presionamos ENTER
><br><br>![git reflog](images/git-reflog.png)<br><br>
><br> *&nbsp;El caracter ^ se obtiene en configuración de teclado ingles con SHIFT + 6 y presionamos la tecla de espacio 
><br> ** `git reset --soft` conserva los cambios 
><br> *** `git reset --mixed` regresa en el tiempo, mantiene los cambios y saca los archivos del stage 
><br> **** `git reset --hard` regresa en el tiempo y elimina los cambios 



>## Mover archivos con git, renombrar y eliminar
>- Para mover un archivo de un path a otro con git introducimos el siguiente comando `git mv nombre_archivo.html htmls/nombre_archivo.html` y presionamos ENTER
>- Al igual si deseamos renombrar el archivo al mismo tiempo introducimos el siguiente comando `git mv nombre_archivo.html htmls/nuevo_nombre_archivo.html` y presionamos ENTER
>- Al igual si deseamos renombrar el archivo y dejarlo en el mismo path con el siguiente comando `git mv nombre_archivo.html nuevo_nombre_archivo.html` y presionamos ENTER
>- Para eliminar un archivo con git introducimos el siguiente comando `git rm nombre_archivo.html` y presionamos ENTER
><br><br>* Con estas acciones se agrega al stage dicho archivo para que nosotros creemos un nuevo commit



## Git ignore
>- Cuando no queremos darle seguimiento a una carpeta o archivo generamos un archivo llamado **.gitignore** en la raíz del proyecto, el lugar donde se encuentra nuestro archivo **.git**
><br ><br >![gitignore](images/gitignore-1.png)<br >
><br >
>- En dicho archivo ingresamos los nombres de todos los archivos y carpetas que deseamos ignorar en git
><br >![gitignore](images/gitignore-2.png)<br >



## Ramas, uniones, conflictos y tags
>- Se recomienda trabajar en ramas nuevas funcionalidades de nuestros desarrollos
>- Para crear una rama en git introducimos el siguiente comando `git branch nombre_de_la_rama` y presionamos ENTER
>- Para ver todas nuestras ramas, incluida la que acabamos de crear `git branch` y presionamos ENTER
>- Para movernos a una rama `git checkout nombre_de_la_rama` y presionamos ENTER