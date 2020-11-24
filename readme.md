**11) Deshacer el último commit (perdiendo los cambios realizados en el working copy)**

Usé el comando 'git reset --hard HEAD~1' para moverme al commit anterior y el modificador 
hard para modificar mi working copy al estado del commit anterior.

**12) Rehacer el último commit (el que acabamos de deshacer)** 

Usé el comando 'git reflog' para poder ver el hash del commit inalcanzable que deshice y 
mediante 'git reset --hard' + hash del commit (2b17774) para regrsar al commit y
modificar mi working copy tal cual estaba en ese commit.

**13) Hacer un merge con ‘master’ (styled absorbe a master)**

No se puede hacer un merge a master porque ya tiene la rama styled absorbido el commit
de master. "Already up to date".

**19) Hacer un merge de “htmlify” en “styled” (styled absorbe a htmlify)**

Se produjo un conflicto al absorber styled a htmlify porque en las dos ramas hemos 
modificado el mismo archivo en las mismas lineas.

**21) Desde “master”, hacer un merge con “styled”**

Cambio a master con git
En este causó no se produjo ningun conflicto porque la rama styled ya contenia a master.
Solamente se movera la rama master al commit de la rama de styled. Por lo que se hizo un
merge fast-forward.

**25) Dibujar el diagrama**

Usé 'git log --graph' para dibujar el diagrama con el log.

**26) Hacer un merge “no fast-forward” de “title” en “master” (master absorbe a title)**

Usé el comando 'git merge --no-ff title' ya que puede ser fast-forward porque title tenia 
los mismo commits que master además de el suyo. Por lo que master avanzo hasta su commit 
absorbiendo esecommit.

**27) Deshacer el merge (sin perder los cambios del working copy)**

Usé 'git reset HEAD~1' para volver al commit anterior a master sin perder los cambios del 
working copy. Lo compruebo con git status

**28) Descartar los cambios**

Úse el comando 'git restore git-nuestro.md' para descartar los cambios.

**29) Eliminar la rama “title”**

Usé 'git branch -D title' para borrar la rama title.

**30) Rehacer el merge que hemos deshecho**

Usé el comando 'git reflog' para buscar el commit donde estaba title (fca534a). Me muevo
a ese commit con 'git checkout' + hash, vuelvo a crear la rama title con 'git branch title'. 
Me cambio a la rama master con 'git checkout master' y hago un merge con 'git merge title'.

**32) Volver al commit inicial cuando se creó el poema**

Mediante el comando 'git log' par ver el primer commit y con 'git checkout' + el hash (954705c)
puse el Head apuntando a ese commit.

**33) Volver al estado final, cuando pusimos título al poema**

Utilizo 'git checkout master' para volver a master que tiene el titulo del poema.
Me aseguro comprobando el contenido del archivo "git-nuestro.md" mediante el comando 
cat git-nuestro.md
