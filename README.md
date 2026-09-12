
**Olaf Herrera Silguero**
***2630250***

# Creación y sincronización de repositorios con Git y GitHub
## Objetivo:
Crear un repositorio local utilizando Git, sincronizarlo con un repositorio remoto en GitHub y comprobar el flujo de trabajo en ambos sentidos:

**Repositorio local → GitHub** 

**GitHub → Repositorio local**

# Descripción del procedimiento realizado
1. CREAR EL REPOSITORIO LOCAL
* Primero creé una carpeta en PowerShell con el nombre **practica-git-olaf-herrera**
* Entre a la carpeta e inicie el repocitorio con el comando `git init` y creé en el repositorio dos archivos:
    * README.md  
    * datos.txt 
* En el archivo datos.txt escribi ***Creé el repositorio Local***
* Luego empece a crear mi primer commit 
* utilice el comamdo `git status`para verificar si los documentos estaban en Untracked file 
* despues los pase al  área de preparación utilisando el comando `git add .`
* luego realice el comando `git commit -m "Primer commit"` para crear el primer commit
---
2. CREAR EL REPOSITORIO EN GITHUB
* Entre en mi navegador a GitHub y creé un repositorio publico nuevo con el mismo nombre
* Copie la URL del repositorio de GitHub para poder vincular el repositorio local con el repositorio remoto con el comando `git remote add origin  git@github.com:Olaf-Herrera/practica-git-Olaf-Herrera.git`
* Verifique que el repositorio remoto se haya agregado correctamente con el Comando `git remote -v`
* Enviel el repositorio local a GitHub con el Comando `git push -u origin main`
* Entre a GitHub y verificar que los archivos aparezcan correctamente
---
3. REALIZAR UN CAMBIO DESDE GITHUB

* Desde la página de GitHub, editar directamente el archivo:
    * datos.txt

* Agrege una nueva línea indicando:
    * Este archivo fue modificado desde GitHub.

* Guarde el cambio realizando un commit desde GitHub y regrese al repositorio local utilizando PowerShell.

* Descargar los cambios realizados en GitHub con el Comando `git pull origin main`

* Abrí datos.txt y verificar que el cambio realizado desde GitHub también aparezca en la computadora.
---
4. REALIZAR UN CAMBIO DESDE EL REPOSITORIO LOCAL
* Modifique nuevamente el archivo datos.txt desde la computadora Agregando una nueva línea indicando:
    * Este archivo fue modificado desde el repositorio local.
* despues agrege los cambios con `git add` y luego `git commit -m "Actualización desde repositorio local"` para crear el nuevo commit
* Envie los cambios a GitHub con el comando `git push`
* volvi a GitHub para verificar los cambios
---
# Comandos de Git utilizados
```bash 
git init
git branch -M main
git status
git add .
git commit -m "Primer commit"
git remote add origin URL_DEL_REPOSITORIO
git remote -v
git push -u origin main
git pull origin main
git commit -m "Actualización desde repositorio local"
git push
```

Explicación breve de la función de cada comando

---
# Explicación de cómo se creó el repositorio local
Se crea una carpeta en PowerShell con el nombre **practica-git-nombre-apellido** para luego entrar e inicir el repocitorio con el comando `git init`
---
# Explicación de cómo se vinculó el repositorio local con GitHub
Se crea un repositorio en GitHub para luego copiar el URL, entrar a la terminal y poner desde el repositorio local `git remote add origin URL_DEL_REPOSITORIO` y con `git remote -v` para Verificar que el repositorio remoto se haya agregado correctamente
---
# Explicación de la sincronización Local → GitHub
Con el Comando `git push -u origin main` el repositorio local se envia a GitHub. Para subir cambios se requiere preparar los cambios con `git add .` o `indicando la ruta del archivo específico` se agragan a la zona Staging Area, se guardar el Commit con `git commit -m "Mensaje descriptivo"`, despues utiliza el comado `git push` para subirlo
---
# Explicación de la sincronización GitHub → Local
Descargar los cambios que se hicieron directamente en GitHub hacia tu computadora se utiliza el Comando `git pull origin main`
---
# Descripción de los archivos contenidos en el repositorio
### En el archivo **README.md** contiene:
```
Informacion para crear un repositorio .git de manera local y como vincularlo a GitHub. Tambien los paso para subir y descargar los cambios del repositorio.
```
### Y en el archivo **texto.txt** contiene:
```
Es una practica para ver como se subia y editada en el repositorio local y en el de GitHub 
```
---