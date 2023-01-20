# Clase 03

## Herramientas con interfaz gráfica

Git Kraken <https://www.gitkraken.com/>
Git Desktop <https://desktop.github.com/>

## RAMAS (Branches) Continuación...

### GIT SWITCH (Cambiar entre ramas)

```sh
git switch <rama>
```

> Para cambiarme entre la rama actual y la anterior

```sh
git switch -
```

> Para crear una rama y moverse a ella en un solo comando

```sh
git switch -c <nombre-de-la-rama>
```

> Ayuda del comando switch 

```sh
git switch --help
```

## Subir una rama al remoto.

```sh
git push -u <alias-remoto> <rama-que-quiero-subir> ## git push --set-upstream origin <rama-que-quiero-subir>
git push -u origin dev
```

## GIT FETCH: Traerme metadata del repo remoto
O sea sicronizar la carpeta .git local con la .git remoto

```sh
git fetch 
git fetch --all
```

## Ver todas las ramas disponibles, incluidas las del remoto en forma detallada
O sea sicronizar la carpeta .git local con la .git remoto

```sh
git branch -av # dónde -a es all y -v es verbose 
```

## Puedo traerme los cambios de una rama en particular

```sh
git pull # Estando en la rama que quiero actualizar. O sea si estoy en dev, se va a actualizar con el remoto, dev
git pull origin dev # No importa sobre que rama estoy, puedo indicarle que sincronizar.
git pull origin feature 
```

# GIT STASH
Es una pila de almacenamiento que provee GIT. 
Permite registrar temporalmente los cambios del WD y del SA.


![GIT STASH](_ref/git_stash.png)


## Ver los stash

```sh
git stash list
```

## Enviar al stash

```sh
git stash # Envia todo lo que esta en el WD, menos los untracked y lo que esta en SA
git stash -u # Si quiero incluir los archivos untracked tengo que poner -u
``` 

## Desapilar o aplicar el último stash

```sh
git stash pop # aplica y borra el último stash
```

## Aplicar o desapilar un stash en particular

```sh
git stash apply # igual pop (aplica el último) pero sin borrarlo
git stash apply stash@{1}
```

## Borrar un stash en particular

```sh
git stash drop # borra el último stash
git stash drop stash@{3}
```

## Ver el contenido del stash

```sh
git stash show -p stash@{1} #Le indico que stash quiero ver
```

## Crear una rama a partir de un stash

```sh
git stash branch <rama-donde-quiero-guardar-lo-que-tengo-en-el-stash>
``` 

## git commit con enmendado(agregado de data faltante en el último commit)

**IMPORTANTE:** Eso debe hacerse SOLAMENTE con el último commit. Ni hablar si trabajo colaborativamente

1. Agregar lo que me falto en el último commit al SA

```sh
git add <archivo-o-archivos>
```

2. Luego hacer un commit  pero con el flag --amend

```sh
git commit --amend
``` 

# Tags (Etiquetas)
Me permite etiquetar commits. 

## Listar todos los tags

```sh
git tag
``` 

## Crear un tag

```sh
git tag <nombre-de-tag> <HASH>
git tag ultimo-commit db3538a
## Version anotada. 
git tag -a v1.0.0 <HASH> -m "<mensaje informativo>"
git tag -a v1.0.0 495e2db -m "Version 1.0.0 - Comenzamos con la clase 03 donde vimos fetch, stash, amend y tags"
```

## Mostrar informaicón detallada de un tag

```sh
git show v0.1.0
```

## Subir un tag en particular

```sh
git push origin <nombre-tag>
```

## NO ES BUENA PRACTICA: Subir todos los tag

```sh
git push --tags
```

## Mostrar el log desde un tag para atrás

```sh
git log v0.1.0 --oneline
```
