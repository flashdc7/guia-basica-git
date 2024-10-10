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
>- Presionamos `ESC`, después escribimos `:wq!` y presionamos `ENTER`

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

![git init](git-init.png)

#### Restaurar un proyecto a como estaba al último commit
- `git checkout -- .`

 