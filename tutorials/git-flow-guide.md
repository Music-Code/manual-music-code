En este tutorial veremos cuáles son los comandos báiscos de GitFlow y que no servirán para poder colaborar todos sobre el repositorio del proyecto

# Primeros Pasos

1. Creamos una carpeta en local que se llame music-code.
2. vamos al github de la organización y elegimos el repositorio que deseamos clonar. Por ejemplo "backend"
3. Copiamos la url del repositorio
4. En la terminal sobre la carpeta music-code

```GIT
git clone https://github.com/Music-Code/backend.git
```

Ahora ya aparecerá nuestro repositorio en local y con la configuración del repositorio.

Al abrir el repositorio podríamos pensar que sólo nos bajamos la rama principal (main) puesto que si ejecutamos el comando git branch sólo nos lista la rama main.

En realidad no es la única que nos ha bajado. El comando git branch, si lo lanzamos sin parámetros, nos lista las ramas locales. Pero si le pasamos el parámetro --all (o -a), nos mostrará tanto las locales como las remotas:

```GIT
git branch -a
```

Esas ramas remotas que vemos en el listado son copias locales de las ramas remotas. Como acabamos de hacer un git clone, esas copias estarán exactamente igual que en el repositorio remoto. Si queremos crear las correspondientes ramas locales, sólo tenemos que ir a cada una de las ramas, en este caso vamos a ir a "develop"

```GIT
git branch checkout develop
```

A partir de ahí podemos crear nuestras nuevas ramas

# Creación Ramas

- **main** viene por defecto una vez creado el repositorio
- **develop** se crea y **SOLO SE CREA UNA VEZ**

### Inicia el repositorio y crea las ramas _main_ y _develop_

```GIT
git flow init
```

> Se ejecuta solo una vez al inicio del proyecto

## feature

### Crea una nueva rama para un feature a partir de la rama _develop_

```GIT
git flow feature start users_add-user
```

A la rama creada se le agrega el tipo feature automaticamente. En este ejemplo el nombre final de la rama sería feature/users_add_user

> users_add_user solo **es un ejemplo** del nombre de la rama

### Terminar un feature y unirla a develop

```GIT
git flow feature finish users_add_user
```

## Hotfix

Inicia una rama hotfix a partir de _main_

```GIT
git flow hotfix start users_add_user
```

A la rama creada se le agrega el tipo hotfix automaticamente. En este ejemplo el nombre final de la rama sería hotfix/users_add_user

Terminar un hotfix y unirlo a las ramas _main_ y _develop_

```GIT
git flow hotfix finish users_add_user
```
