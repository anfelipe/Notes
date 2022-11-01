# **Git**

### **¿Qué es?**
*Git es un sistema de control de versiones pensado para aplicaciones que generalmente tienen un número grande de archivos.*

<img src="./Images/Git/git_icon.svg" width="40">

[Git](https://git-scm.com) - *página principal de Git.*
<br/>

### **¿Qué es un sistema de control de versiones?**
*Es un sistema que registra los cambios realizados sobre un archivo a lo largo del tiempo; Permite comparar cambios, ver quien realizó cada uno de esos cambios y si es el caso, obtener una versión anterior de un archivo.*

### **¿Qué es Github?**
*Es una plataforma para alojar proyectos utilizando Git. "Es donde vas a ver todos los archivos de tu aplicación en la nube".*

<img src="./Images/Git/github_icon.svg" width="40">

[GitHub](https://github.com/) - *página principal de GitHub.*

### **¿Qué es Git Bash?**
*Es una consola que nos permite correr commandos de Linux para trabajar con Git.*

<br/>

# **Conceptos de Git**

#### **Repository**
<img src="./Images/Git/git_repository_icon.svg" width="40">
Donde se almacena todo el proyecto, el cual puede vivir tanto en local como en remoto. El repositorio guarda un historial de versiones y, más importante, la relación de cada versión con la anterior para que pueda hacerse el árbol de versiones con las diferentes ramas.

<br/>

### **Clone**
<img src="./Images/Git/git_clone_icon.svg" width="40">
Para poder trabajar en un proyecto existente, se clona el repositorio al computador personal.

<br/>

### **Branch**
<img src="./Images/Git/git_branch_icon.svg" width="40">
Es una rama, bifurcación o copia del proyecto, que ayuda a mantener un orden en el control de las versiones.

<br/>

### **main**
<img src="./Images/Git/git_master_icon.svg" width="40">
Rama donde se almacena la última versión estable del proyecto. Es donde todo funciona y sirve como referente para nuevas ramas o branch.

<br/>

### **Commit**
<img src="./Images/Git/git_commit_icon.svg" width="40">
Comando de consola que consiste en confirmar cambios en la versión local del repositorio, "Haces commit cuando das por terminado el trabajo en uno o varios archivos". Esto crea una nueva versión de los archivos incluidos en el commit.

<br/>

### **Push**
<img src="./Images/Git/git_push_icon.svg" width="40">
Consiste en enviar todo lo que se ha confirmado con un commit al repositorio remoto. Aquí es donde se une nuestro trabajo con el de los demás.

<br/>

### **Checkout**
<img src="./Images/Git/git_checkout_icon.svg" width="40">
Commando que sirve para crear, descargar y movernos entre ramas o los cambios que se especifiquen, del repositorio GIT local o remoto. Tambien nos permite volver a una versión anterior de un archivo o del proyecto.

<br/>

### **Fetch**
<img src="./Images/Git/git_fetch_icon.svg" width="40">
Comando que actualiza el repositorio local bajando datos del repositorio remoto al repositorio local sin actualizarlo, es decir, se guarda una copia del repositorio remoto en el local.

<br/>

### **Merge**
<img src="./Images/Git/git_merge_icon.svg" width="40">
El merge permite unir ramas o la copia del repositorio remoto con tu repositorio local, mezclando los diferentes códigos.

<br/>

### **Pull** 

Consiste en la unión del fetch y del merge, esto es, recoge la información del repositorio remoto y lo mezcla con el trabajo en local.

<br/>

### **Diff**
<img src="./Images/Git/git_diff_icon.svg" width="40">
Se utiliza para mostrar los cambios entre dos versiones del mismo archivo.

<br/>

### **Pull Request**
<img src="./Images/Git/git_pull_request_icon.svg" width="40">
Funcionalidad de GitHub conocida tambien como (PR), en la que un colaborador pide que revisen los cambios antes de hacer merge a una rama (master).

<br/>

### **Fork**
<img src="./Images/Git/git_fork_icon1.svg" width="40">
Si en algún momento queremos contribuir al proyecto de otra persona, o si queremos utilizar el proyecto de otro como el punto de partida del nuestro. Esto se conoce como “fork”.


<br/>

# **Ciclos de vida**
Son estados por los que puede pasar un archivo según la forma en que se manipule.

### **Untracked**
Estado donde los archivos que están en el disco duro, es decir que no se han agregado con `git add`.

### **Tracked**
Estado de rastreo para los archivos que han sido agregados con `git add`.

### **Staged**
Estado donde se almacenan temporalmente los archivos en memoria RAM con el comando `git add` antes de agregarlos al repositorio con `git commit`. Es un estado intermedio de preparación antes de pasar al repositorio.

### **Unstaged**
Estado donde los archivos que no están incluidos del todo en el ***Staged*** pero se les sigue haciendo seguimiento ***Tracked***.

<br/>


# **Comandos de Git**

### **git init**

Comando que inicia un nuevo repositorio en el directorio donde estas.

```
git init
```

Adicional se crea una carpeta oculta llamada `.git` donde se va a almacenar los cambios en el proyecto.

### **git config**
Comando para ver las configuraciones de `git`.

```
git config                          //Configuraciones
git config --list                   //Configuraciones hechas
git config --list --show-origin     //Configuraciones y rutas
```

### **git status**
Comando para ver el estado de los archivos, es decir indica que haz agregado al staged o que falta por agregar.

```
git status
```

### **git add**
Comando para enviar uno o todos los archivos al staged. Los archivos que se envian son los nuevos, modificados y eliminados.

```
git add nombre_archivo    //Enviar un archivo en especifico
git add .       //Enviar todos los archivos de la carpeta actual
```

### **git rm**
Comando para eliminar un archivo del staged o del repositorio sin eliminar su historial.

```
git rm --cached nombre_archivo      //Elimina del staging
git rm --force             //Elimina del staged y del disco duro
git rm nombre_archivo      //Elimina del repositorio
```

### **git commit**
Comando para enviar los cambios al repositorio (local). ""

```
git commit -m "Mensaje del commit"
git commit -am "Mensaje del commit" //ejecuta git add + git commit
```

### **git push**
Comando que envia los archivos a un reposotorio remoto. Se envian los archivos a los que se les hizo commit `git commit`.

```
git push
```

### **git reset**
Comando que devuelve los cambios a su estado anterior. 

```
git reset HEAD nombre_archivo //Saca los archivos del staging

git reset [commit] --soft //borra los cambios en el directorio pero los deja en el staged

git reset [commit] --mixed //borra hasta en el directorio

git reset [commit] --hard //borra hasta el mismo commit
```

### **git pull**
Comando para traer un repositorio remoto al local.

```
git pull
```

### **git diff**
Comando que compara un archivo entre dos versiones.

```
git diff commitV1 commitV2
```

### **git log**
Comando para ver el historial de un archivo.

```
git log nombre_archivo
git log --oneline   //Muestra el id commit y el título
git log --decorate  //Muestra donde está el head point
git log > log.txt   //Guarda los logs en un archivo .txt
```

[Atlassian](https://www.atlassian.com/git/tutorials/git-log?msclkid=0f9de9a2c81011eca81ca5418fef3a75) - *Mas usos de `git log`*

### **git branch**
Comando para crear una nueva rama de donde estoy parado.

```
git branch nombre_rama
git branch -d   //Borra rama
```

### **git checkout**
Comando para ir a una versión especifica de un proyecto o archivo.

```
git checkout [commit] nombre_archivo //salta al commit indicado
git checkout main //salta a la rama main
git checkout -b nombre_rama //Crear una rama y nos mueve a ella
```

### **git merge**
Comando para fusionar cambios entre la rama donde estas parado y la rama que se indica. *"los merge tambien son commits".*

```
git merge nombre_rama
git merge --abort   //revierte el merge
```

### **git remote**
Comando para conectar un repositorio remoto con el local.

```
git remote add origin url_repositorio_remoto
git remote -v //verifica la url del repositorio remoto
```

una vez se hace el git remote se deben bajar los cambios del repositorio remoto y hacer *merge* con el local, para esto se usa el comando `git pull origin main --allow-unrelated-histories`.

Para subir los cambios al repositorio remoto ya enlazado se debe ejecutar el comando `git push origin main`.

### **gitignore**
Es un archivo donde se especifica que archivos van a ser ignorados y no van a subir al repositorio remoto.
[gitignore](https://git-scm.com/docs/gitignore). Normalmente se descartan archivos binarios, carpeta de compilación y configuraciones que contengan contraseñas.

### **Tags**
Permiten asignar una etiqueta o versión a los commits, normalmente se asignan a los que tienen un nivel de importancia significativo.

*Crear un Tag*
```
git tag -a nombre_tag -m "descripcion_tag" id_commit
```

*Listar Tag local*
```
git tag
git show-ref --tags
```

*Borrar Tag*
```
git tag -d nombre_tag
```

*Publicar Tag a repositorio remoto*
```
git push origin --tags
```

*Borrar Tag de repositorio remoto*
```
git tag -d nombre_tag
git push origin :refs/tags/nombre_tag
```