# Clase 02

## .gitkeep
Hace que git pueda versionar una carpeta vacía. Porque git no reconoce las carpetas si no tienen dentro un archivo.

Crear en la carpeta vacía un archivo llamado **.gitkeep**

## .gitignore
Me permite descartar o omitir archivos y carpetas para que no sean tenidos en cuenta por git.

En raíz tengo que crear un archivo **.gitignore** y dentro colocar las carpetas o archivos que quiero ignorar

# Subiendo el repo local al remoto

1. Creo el repo en Github
2. Elijo HTTP
3. Ejecuto el comando siguiente:


```sh
git remote add <alias> <url>
git remote add origin https://github.com/mlapeducacionit/64289.git # Agrega el repo remoto al local
```

```sh
git push -u <alias> <rama>
git push -u origin main # -u: --set-upstream | Sube el repositorio local al remoto.
``` 

> Una vez configurado el remoto y asociada la rama local con la rama remota

```sh
git push
```

# GIT BRANCH (RAMAS)

## Crear una rama

```sh
git branch <nombre-rama>
git branch ramas
```

## Para ver las ramas disponibles

```sh
git branch
```

## Cambiarme de ramas

```sh
git switch <nombre-rama>
git switch ramas
```

# Borrar ramas 

> Borrar ramas que ya están fusionadas

```sh
git branch -d <nombre-rama>
git branch -d fusiones
```

> Borrar ramas que nunca se funsionaron

```sh
git branch -D <nombre-rama>
git branch -D fusiones
```
# GIT MERGE
IMPORTANTE: Tengo que estar en la rama en la cual quiero recibir los commits. O sea que si quiero traerme los cambios de la rama fusion a la main. Tengo que estar parado en la rama main y ejecutar el comando siguiente:

```sh
git merge <nombre-de-rama>
git merge funsion
```

## Tenemos 3 tipos diferentes de fusiones

* Fast-fodward (No hay ningun conflicto, o sea que no hay líneas que se superponen entre si entre las diferentes ramas)

* Recursiva (Tiene diferentes algoritmos de fusión. Lo solucion git solo también.)

* Manual (Conflictos - Ocurre cuando hay modificaciones en las misma líneas de código)

NOTA: Al solucionar el conflicto en la fusión manual para confirmar tengo que hacer un commit.

## Cancelar la fusión

```sh
git merge --abort
```

## Fusionar varias ramas

```sh
git merge <rama1> <rama2>
```
Nota: Estando en main trae el contenido de las rama1 y la rama2



## Configurar la conexión por SSH
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent


