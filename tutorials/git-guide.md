En este tutorial veremos cuáles son los comandos báiscos de Git y que no servirán para poder colaborar todos sobre el repositorio del proyecto

# Primeros Pasos

1. Creamos una carpeta en local que se llame music-code.
2. vamos al github de la organización y elegimos el repositorio que deseamos clonar. Por ejemplo "backend"
3. Copiamos la url del repositorio
4. En la terminal sobre la carpeta music-code

```GIT
git clone https://github.com/Music-Code/backend.git
```

Ahora ya aparecerá nuestro repositorio en local y con la configuración del repositorio.

# Creación Ramas

- **main** viene por defecto una vez creado el repositorio
- **develop** se crea y **SOLO SE CREA UNA VEZ**

```GIT
# Creamos la rama y nos movemos a ella
# Ya está creada
git checkout -b develop

# Subir rama al github
git push -u origin develop

```

- **feature**

```GIT
git checkout -b feature/user_add_user

# De otro forma
git switch -c feature/user_add_user
```

> Recuerde que se debe estar en la rama develop para crear un feature

### Comprobar las ramas que tenemos

```GIT
git branch
```

### Moverse a otras ramas

```GIT
git switch nombre_rama

# De otro forma
git checkout nombre_rama
```

<!-- ### Ver si tenemos la última actualización -->
<!--
Si deseamos que la rama feature/user_add_user nos diga si se ha realizado cambios en develop que pueden afectarnos debemos hacerle seguimiento a la rama develop desde la rama feature/user_add_user

```GIT
git branch --set-upstream-to=origin/develop feature/user_add_user
```

Una vez hecho el seguimiento se puede comprobar si ha habido cambios

```GIT
git pull
```

> Revisad que siempre estemos en la rama correspondiente y nunca en **main** o **develop** a no ser que sea estrictamente necesario. -->
