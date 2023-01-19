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


## Configurar la conexión por SSH
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent


