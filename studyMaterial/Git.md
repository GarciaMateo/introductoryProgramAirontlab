Git 

Git es un sistema de control de versiones. El control de versiones, también conocido como "control de código fuente", es la práctica de rastrear y gestionar los cambios en el código de software.
Realiza un seguimiento de todas las modificaciones en el código en un tipo especial de base de datos. Si se comete un error, los desarrolladores pueden ir hacia atrás en el tiempo y comparar las versiones anteriores del código para ayudar a resolver el error, al tiempo que se minimizan las interrupciones para todos los miembros del equipo.
Funcionamiento
Inicialización del repositorio central
En primer lugar, hace falta crear el repositorio central en un servidor. Si se trata de un proyecto nuevo, puedes inicializar un repositorio vacío. Si no es así, tendrás que importar un repositorio Git existente.

Configuración de un repositorio
- git clone:se utiliza principalmente para apuntar a un repositorio existente y clonar o copiar dicho repositorio en un nuevo directorio, en otra ubicación.
- git init: crea un nuevo repositorio de Git. Se crea un subdirectorio de .git en el directorio de trabajo actual, que contiene todos los metadatos de Git necesarios para el nuevo repositorio.
- git init --bare <directory>:Inicializa un repositorio de Git vacío, pero omite el directorio de trabajo. Los repositorios compartidos deberían crearse siempre con la marca --bare.

Aplicación de cambios y confirmaciones
- git status: muestra el estado del directorio de trabajo y del área del entorno de ensayo. Permite ver los cambios que se han preparado, los que no y los archivos en los que Git no va a realizar el seguimiento.
- git add: agrega un cambio en el directorio de trabajo al área de ensayo. Le dice a Git que desea incluir actualizaciones de un archivo en particular en la próxima confirmación.
- git commit: captura una instantánea de los cambios preparados en ese momento del proyecto.

Sincronización de Git

- git remote: te permite crear, ver y eliminar conexiones con otros repositorios. 
- git fetch: descarga commits, archivos y referencias de un repositorio remoto a tu repositorio local. Esta acción la llevas a cabo cuando quieres ver en qué han estado trabajando los demás.
- git push se usa para cargar contenido del repositorio local a un repositorio remoto.Es el equivalente a git fetch, pero mientras que al recuperar se importan las confirmaciones a ramas locales, al enviar estas se exportan a ramas remotas.
git pull se emplea para extraer y descargar contenido desde un repositorio remoto y actualizar al instante el repositorio local para reflejar ese contenido.

Uso de ramas

El comando git branch te permite crear, enumerar y eliminar ramas, así como cambiar su nombre. No te permite cambiar entre ramas o volver a unir un historial bifurcado. Por este motivo, git branch está estrechamente integrado con los comandos git checkout y git merge.
- git branch:Enumera todas las ramas de tu repositorio. Es similar a git branch --list.
- git branch <branch>:Crea una nueva rama llamada ＜branch＞. Este comando no extrae la nueva rama.
- git branch -d <branch>:Elimina la rama especificada. Esta es una operación segura, ya que Git evita que elimines la rama si tiene cambios que aún no se han fusionado.
- git branch -D <branch>:Fuerza la eliminación de la rama especificada, incluso si tiene cambios sin fusionar.
- git branch -m <branch>:Cambia el nombre de la rama actual a ＜branch＞.
- git branch -a: Enumera todas las ramas remotas.
- git merge: Permite tomar las líneas independientes de desarrollo creadas por git branch e integrarlas en una sola rama.
- git checkout: te permite desplazarte entre las ramas creadas por git branch.
- git checkout -b ＜new-branch＞: creará la nueva rama y cambiará a ella al instante
- git checkout -b ＜new-branch＞ ＜existing-branch＞: se añade ＜existing-branch＞, que basa new-branch en existing-branch y no en el HEAD actual.
