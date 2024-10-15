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



 >## ****** GIT NO LE DA SEGUIMIENTO A CARPETAS VACIAS ******
 >- Para mantener un directorio vacio en nuestro repositorio que sabemos que necesitamos en nuestro proyecto solo agregamos dentro del directorio el siguiente archivo **.gitkeep**
 


>## Creación de ALIAS para nuestros comandos
>- Son versiones cortas de los comandos de git, para crear un alias escribimos el siguiente comando `git config --global alias.nombre_del_alias seguido de los comandos que deseamos agregar entre comillas`
>- Ej `git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"` 
>- Para modificar un alias tecleamos el siguiente código `git config --global -e`
><br><br>![git alias](images/alias.png) <br><br>
>- Una vez que terminamos la edición presionamos ESC después :wq!
>- Y a continuación corremos nuestro alias y se vería de la siguiente forma
><br><br>![git alias](images/alias-lg.png) <br><br>



