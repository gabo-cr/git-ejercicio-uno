# Ejercicio 1

- **¿Qué comando utilizaste en el paso 11? ¿Por qué?**

    Usé el comando `git reset --hard HEAD~1`. Porque al hacer `reset`, el puntero se mueve hacia el commit que se indica como `HEAD~1`, es decir, al penúltimo commit. Y al añadirle la opción `--hard`, se pierden los cambios realizados en el working copy.

- **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

    Primero hice un `git reflog`, para revisar los pasos que había realizado en el repositorio local y encontrar el identificador del commit hacia el que quería regresar. Luego, hice `git reset --hard 713f738`, donde usé `reset` para mover el puntero hacia el commit con el identificador `713f738` y le añadí la opción `--hard` para que también me devuelva los cambios en el working copy.

- **El merge del paso 13, ¿causó algún conflicto? ¿Por qué?**

    El merge de la branch `styled` con la branch `main` no causó ningún conflicto, porque la branch `styled` solo contenía un commit más de los que ya contenía la branch `main`, por lo que al absorberla no había nada nuevo que absorber.

- **El merge del paso 19, ¿causó algún conflicto? ¿Por qué?**

    Sí, porque tanto en la branch `styled` como en la branch `htmlify` se hicieron varios cambios en las mismas líneas del archivo git-nuestro.md.

- **El merge del paso 21, ¿causó algún conflicto? ¿Por qué?**

    No, porque los cambios que estaban en la branch `styled` fueron añadidos encima de lo que tenía la branch `main`, por lo que al hacer el merge solo se actualiza la branch `main` con esos nuevos cambios.

- **¿Qué comando o comandos utilizaste en el paso 25?**

    Para dibujar el diagrama usé `git log --graph` para ver el diagrama detallado y `git log --graph --oneline` para verlo condensado.

- **El merge del paso 26, ¿podría ser fast forward? ¿Por qué?**

    Sí, pudo haber sido un merge fast forward, porque la branch `main` seguía en el mismo commit a partir del cual se creó la branch `title`, por lo cual solo se hubiese actualizado la branch `main` actualizando el puntero para que apunte al mismo commit al que estaba apuntando la branch `title`.

- **¿Qué comando o comandos utilizaste en el paso 27?**

    Primero usé el comando `git log` para encontrar el commit (dentro de la branch `main`) previo al merge hacia donde quería volver. Luego usé `git reset 1db558545357054049674d2f71f3c7f9593e36ff` para volver a ese commit y no perder los cambios del working copy.

- **¿Qué comando o comandos utilizaste en el paso 28?**

    Usé `git restore git-nuestro.md` para descartar los cambios en el working copy hechos en el archivo git-nuestro.md.

- **¿Qué comando o comandos utilizaste en el paso 29?**

    Usé `git branch -D title` para eliminar la branch `title`.

- **¿Qué comando o comandos utilizaste en el paso 30?**

    Primero hice un `git reflog`, para revisar los pasos que había realizado en el repositorio local y encontrar el identificador del commit hacia el que quería regresar. Luego usé `git reset --hard c88d854` para rehacer el merge y volver a tener los cambios en el working copy.

- **¿Qué comando o comandos utilizaste en el paso 32?**

    Primero usé `git log` para conocer el identificador del commit inicial. Luego usé `git reset a840a4891170b8d51d8e3515f63c26d604c0cdec` para volver a dicho commit inicial. No añadí la opción `--hard`, porque el enunciado no especificaba si debía o no perder los cambios en el working copy.

- **¿Qué comando o comandos utilizaste en el paso 33?**

    Primero usé `git reflog` para encontrar el identificador del commit del estado final, donde pusimos el título del poema. Luego usé `git reset c88d854` para volver a dicho commit final. No añadí la opción `--hard`, porque aún tenía los cambios en el working copy, por lo que no hacía falta recuperarlos.
