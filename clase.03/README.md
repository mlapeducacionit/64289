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



