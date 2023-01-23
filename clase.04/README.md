# Clase 04

## Entregas

* Además de los desafios
* Entrega de Integradores en un repo de github
    * HTML
    * C#
    * MYSQL
    * GIT

## Para resolver el desafío del módulo 3

1. Clonar el repo: https://github.com/mlapeducacionit/web-veterinaria
2. agregar en la rama main el **status.js** 
3. crear la rama custom-navbar
4. empezar a trabajar
5. crear el stash para resolver la incidencia que nos piden.

# GIT RESET
Nos permite resetear (volver atrás cambios: volver atraás commits)
Nota: Recuerden que tengo que seleccionar el hash anterior al que quiero hacerle reset.
## SOFT

```sh
git reset --soft <hash>
```

## MIXED

```sh
git reset <hash>
git reset --mixed <hash>
```

## HARD
PELIGROSO. Hay que tratarlo con respeto. Pierdo toda la información.

```sh
git reset --hard <hash>
```

# REFLOG: Mira la historia global del REPO

```sh
git reflog
```
