Alumno 1 -> Antonio Romero Bonilla
Alumno 2 -> Sergio José Bastón Losey

3. Creación e inicialización del repositorio (Alumno 1)
Los comandos utilizados hasta ahora son:
  git init: para inicializar el repositorio git
  git add . : añade los cambios al área de preparación
  git commit -m: añade los cambios al repositorio
  git remote add origin https://github.com/ItzPhoeniX719/GIT_IA_AntonioSergio: para añadir la URL como origen del repositorio
  git push origin master: para subir los contenidos del master al repositorio remoto (origin)

5. Clonar repositorio (Alumno 2)

git clone https://github.com/ItzPhoeniX719/GIT_IA_AntonioSergio: este comando se utiliza para hacer un clon de un repositorio remoto para tener ese repositorio en tu máquina local.

7. Creación de ramas (ambos)
git branch: para listar las ramas y ver en cuál estamos situada
git branch [nombre-de-rama]: para crear una rama con el nombre especificado
git checkout [nombre-de-rama]: para cambiar a la rama con el nombre especificado
git checkout -b [nombre-de-rama]: para crear y al mismo tiempo cambiar a la nueva rama creada
git branch -m [nuevo-nombre]: para renombrar la rama
git diff master [rama-del-alumno]: para comparar las diferencias entre la rama master y la rama del alumno

11. Merge sin conflictos
No, no he podido realizar los pasos del ejercicio de forma completamente idéntica.
El motivo es que, cuando intenté fusionar mi rama personal con master, mi rama master local no estaba sincronizada con la master del repositorio remoto. Otros compañeros ya habían hecho sus merges y pushes previamente, por lo que la historia del repositorio había avanzado.

Como consecuencia, Git detectó que mi master local y la master remota habían divergido, y me pidió que especificara cómo quería resolver esa divergencia: mediante merge o mediante rebase.

Para solucionarlo de forma consistente con el flujo de trabajo del ejercicio, ejecuté:
git config pull.rebase false

Este comando configura Git para que, cada vez que se haga un git pull, se utilice por defecto merge en lugar de rebase. Es decir, Git combinará los cambios remotos con los locales mediante un commit de merge, que es el comportamiento más habitual en proyectos colaborativos como este.

Después de aplicar esta configuración, pude continuar con el merge y completar el ejercicio sin problemas.

12. Credenciales
Usamos el comando git config --global credential.helper store para que la próxima vez que se nos pidan las credenciales estas se guarden y para posteriores push/etc. no nos las vuelvan a pedir.
