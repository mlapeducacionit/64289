# GIT Desarrollo colaborativo

## Clase 01

## Bajar e instalar GIT

<https://git-scm.com/>


## Areas en GIT

* Working Directory (WD): Es el area de trabajo

* Staging Area o Index (SA): Area temporal de confirmación de cambios, previo al commit (Foto del código)

* Local Repo (LR): Caja de commits. Aca voy a tener todos los commits que le vaya haciendo al código.

## Configurar GIT

```sh
git config --global user.name "Nombre Apellido"
git config --global user.email "mlapeducacionit@gmail.com"
```

### Ayuda del comando CONFIG

```sh
git config --help
```

### Listado de configuraciones

```sh
git config --list
```

## Inicializar o crear repo

```sh
git init
```

## Estado de los archivos dentro del repo


* Untracked: Archivos desconocidos por el repositorio

* Unmodified: Archivos conocidos por el repositorio, pero que no sufrieron modificaciones desde el último commit

* Modified: Archivos conocidos por el repositorio, y a su vez, fueron modificados

* Staged: Archivos cuyos cambios fueron confirmados por nosotros

## Agregar a la zona de confirmación (Staging Area o Index)

```sh
git add <nombre-archivo>
git add clase.01/README.md
git add .gitignore
git add index.html
git add . # es comodín que nos permite agregar todo.
```
## Para sacar una foto de nuestros archivos. (Hacer un commit)

```sh
git commit # Abre un editor para escribir el mensaje
git commit -m "Mensaje del contenido del commit" 
```