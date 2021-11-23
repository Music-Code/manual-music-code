En este tutorial veremos cuáles son los comandos báiscos de Git y que no servirán para poder colaborar todos sobre el repositorio del proyecto

# Primeros Pasos
1. Creamos una carpeta en local que se llame music-code.
3. vamos al github de la organización y elegimos el repositorio que deseamos clonar. Por ejemplo "backend"
4. Copiamos la url del repositorio
5. En la terminal sobre la carpeta music-code

```GIT
git clone https://github.com/Music-Code/backend.git
```

Ahora ya aparecerá nuestro repositorio en local y con la configuración del repositorio.

# Creación Ramas

- **main** viene por defecto una vez creado el repositorio
- **develop** se crea y **SOLO SE CREA UNA VEZ**

```GIT
// Creamos la rama y nos movemos a ella
// Ya está creada
git checkout -b develop

// Subir rama al github
git push origin develop

```

- **feature**

```GIT
git checkout -b feat_user_AddUser
```

para subir la rama al github, en caso de que sea necesario 

```GIT
git push origin feat_user_AddUser
```

### Comprobar las ramas que tenemos

```GIT
git branch
```

### Moverse a otras ramas

```GIT
git checkout nombre_rama
```

### Ver si tenemos la última actualización

Si deseamos que la rama feat_user_AddUser nos diga si se ha realizado cambios en develop que pueden afectarnos debemos hacerle seguimiento a la rama develop desde la rama feat_user_AddUser

```GIT
git branch --set-upstream-to=origin/develop feat_user_AddUser
```

Una vez hecho el seguimiento se puede comprobar si ha habido cambios

```GIT
git pull
```




> Revisad que siempre estemos en la rama correspondiente y nunca en **main** o **develop** a no ser que sea estrictamente necesario.








