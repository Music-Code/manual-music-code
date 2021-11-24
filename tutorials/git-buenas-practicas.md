Durante el desarrollo de un proyecto es muy recomendable contar con una guía de buenas prácticas para la creación de ramas y commits. Esta guía pretende ser clara y debe ayudar a cualquier miembro del equipo.

Con esto pretendemos llevar la comunicación y coordinación del equipo de la mejor forma para que el proyecto sea limpio y claro.

# 🌿 Manejo de Ramas

Durante el desarrollo vamos a crear branches/ramas para poder trabajar de manera aislada y poder realizar todos los cambios, correcciones y nuevas características del proyecto sin afectar el flujo de trabajo del resto del equipo, así evitaremos mezclar código de distintas líneas de desarrollo. Para poder gestionarnos bien seguiremos los siguentes estándares y buenas prácticas.

### - Estructura

El nombre de una rama se estructura de 3 partes diferentes el tipo, modulo y característica, estas partes son divididas usando "/" y "\_" como se muestra en nuestra en el ejemplo siguiente.

```GIT
tipo/modulo_caracteristica

```

> Los nombres de las ramas tienen que ser escritos en **snake_case**.

### - Tipo:

El tipo es la primer parte de la estructura de la rama y hace referencia a la acción que se está realizando:

- **feature**: Se generan una nueva funcionalid.
- **hotfix**: Se realizan correción de Bugs que se detectaron en la rema main y deben ser reparados urgentemente.
- **refactor**: Refactorización de funcionalidades y mejoras.
- **docs**: Se generar cambios en la documentación.

### - Módulo:

Segunda parte de la estructura de la rama y hace referencia a sobre qué se está desarrollando. El módulo no debe constar de más de 15 caracteres

### - Característica:

Tercera parte de la estructura de la rama. Este nombre nos indica exacatamente que funcionabilidad del modulo se está desarrollando. Puede ser un nombre subjetivo pero siempre descriptivo. Además no debe superar los los 30 caracteres.

### Ejemplo

```
feature/usuario_update_user
```

# 📌 Manejo de Commits

Los mensajes de commits deben ser claros y ayudar a cualquier miembro del equipo. Debemos evitar que estos mensajes cada vez se vuelven menos informativos y podemos encontrar mensajes como "ya funciona esto" lo cual da lugar mensajes no descriptivos y peor aún en ocasiones ni el responsable recuerda o sabe lo que generó.

Por ello, el mensaje de un commit se divide en 3 partes diferentes el tipo: título, el cuerpo y pie como se muestra en el siguiente ejemplo.

### - Tipo: Título:

El tipo es contenido en el título y puede ser de alguno de los siguientes casos:

- 💫 FEAT: Una nueva característica.
- 🛠️ FIX: Se soluciono un bug.
- 📚 DOCS: Se realizaron cambios en la documentación.
- 🌈 PRETT: Se aplico formato, comas y puntos faltantes, etc; Sin cambios en el código.
- ♻ REFACT: Refactorización del código en producción.
- 🔎 TEST: Se añadieron pruebas, refactorización de pruebas; Sin cambios en el código.
- ☠️ DELETE: Se eliminan funciones o archivos.
- 💚 CHORE: Actualización de tareas de build, configuración del admin. de paquetes; Sin cambios en el código.

**Subject/Asunto**

- Comunica qué hace el cambio sin necesidad de mirar al código fuente
- El asunto no debe contener más de **50 caracteres**,
- Iniciar con una letra mayúscula y
- **NO** terminar con un punto.
- Usa el imperativo al momento de redactar nuestro commit, es decir, hay que ser objetivos.

### - Cuerpo

Usa el cuerpo del mensaje para explicar **"por qué"**, **"para qué"**, **"cómo"** y detalles adicionales.
Por tanto, cuando el por qué de un cambio no quede suficientemente claro con el asunto y el diff del commit, usaremos el cuerpo del mensaje de commit para aportar un contexto y un por qué a dichos cambios. Esto es especialmente importante si existen soluciones alternativas a la implementada en el commit, ya que así los futuros mantenedores del código pueden saber por qué se elegió esa solución frente a otras alternativas.
Si el cambio realizado, además, puede tener consecuencias inesperadas o efectos secundarios en el resto del código, es importante especificarlo también en el mensaje de commit.

- 72 caracteres máximo
- El asunto y el cuerpo del mensaje se separan por una línea en blanco. Las líneas en blanco adicionales pasan a ser consideradas parte del cuerpo del mensaje.

### - Footer

Esta parte es muy importante ya que es donde se coloca el seguimiento de los issues o tickets relacionados con los cambios generados.

- Para poder referencias un issue en el commit siempre se tiene que colocar # seguida del número de issue. Este issue estará relacionado con Trello.

> Escribirlo en **Inglés** es una de las mejores prácticas que podemos tener.

## Ejemplo 1

```GIT
📚 DOCS: Redaccion de reglas para commits.

En la seccion de Wiki se redactaron las buenas prácticas para los commits

Issue: #1

```

## Ejemplo 2

```GIT
💫 FEAT: Summarize changes in around 50 characters or less

More detailed explanatory text, if necessary. Wrap it to about 72
characters or so. In some contexts, the first line is treated as the
subject of the commit and the rest of the text as the body. The
blank line separating the summary from the body is critical (unless
you omit the body entirely); various tools like `log`, `shortlog`
and `rebase` can get confused if you run the two together.

Explain the problem that this commit is solving. Focus on why you
are making this change as opposed to how (the code explains that).
Are there side effects or other unintuitive consequences of this
change? Here's the place to explain them.

Further paragraphs come after blank lines.

 - Bullet points are okay, too

 - Typically a hyphen or asterisk is used for the bullet, preceded
   by a single space, with blank lines in between, but conventions
   vary here

If you use an issue tracker, put references to them at the bottom,
like this:

Resolves: #123
See also: #456, #789

```
