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

# De otra forma
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

### Nuevas ramas remotas durante el proyecto

¿Y si ya tenemos el repositorio clonado, llevamos un tiempo trabajando en él, y un día un miembro del equipo sube una rama nueva al repositorio remoto? ¿Nos tiene que avisar? ¿Tenemos que saber cómo se llama la nueva rama? No es necesario, vamos a ver cómo tener siempre actualizadas las copias locales de las ramas remotas.

una vez que las ramas locales están vinculadas con las remotas, podemos usar git push y git pull sin necesidad de escribir el nombre de una rama. ¿Qué ocurre cuando yo escribo git pull a secas? Sabemos que el comando git pull en realidad lanza dos comandos secuencialmente: primero hace git fetch y luego git merge. Ese primer comando es el que nos interesa: ese fetch nos actualizará todas las copias locales de las ramas remotas, copiando las que haya nuevas. Es decir, cada vez que hacemos un git pull sin nombre de rama, estamos sincronizando nuestras copias de las remotas con las ramas remotas reales.

```GIT
git checkout nombre_rama
```

Para crear la rama local correspondiente, sólo tenemos que entrar en ella, como hacíamos justo después del git clone, y Git nos la creará a partir de la copia remota.

# 📌 AÑADIR COMMITS: GIT ADD

Para el git add **NO** usar '_git add ._' a no ser que sea muy necesario. Lo mejor es usar git add y poner los archivos modificados.

Si ejecutamos

```GIT
git status
```

y obtenemos

```TERMINAL
Cambios no rastreados para el commit:
  (usa "git add <archivo>..." para actualizar lo que será confirmado)
  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
        modificado:     tutorials/git-flow-guide.md
        modificado:     tutorials/git-guide.md

sin cambios agregados al commit (usa "git add" y/o "git commit -a")
user@MacBook-Pro-de-user folder %
```

para agregar los archivos debemos hacerlo así:

```GIT
git add tutorials/git-flow-guide.md tutorials/git-guide.md
```
