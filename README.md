# Este es un repocitorio de ejemplo para aprender a utilizar GIT y GITHub.

Ejercicio 1: Configurar Git con tu nombre y correo
Objetivo: Aprender a configurar Git por primera vez.
Pasos:
Abrir Git Bash (es la consola de Git).


Escribir los siguientes comandos:
git config --global user.name "Tu Nombre"
git config --global user.email "tunombre@ejemplo.com"


3. Verificar que se guardó correctamente con:
git config --global --list
Resultado esperado:
user.name=Tu Nombre
user.email=tunombre@ejemplo.com
=====================================================
Ejercicio 2: Crear un repositorio local con una página HTML
Objetivo: Crear un proyecto básico y versionarlo con Git.
Pasos:
Crear una carpeta nueva llamada mi_pagina en el escritorio.


Dentro de esa carpeta, crear un archivo llamado index.html con este contenido:
<!DOCTYPE html>
<html>
  <head><title>Mi primera página</title></head>
  <body><h1>¡Hola mundo!</h1></body>
</html>
3. Abrir Git Bash en esa carpeta (clic derecho > Git Bash Here) y escribir:
git init
git add index.html
git commit -m "Primer commit: página HTML"


Resultado esperado: Git empieza a seguir el proyecto y guarda el primer cambio.
===============================================================
Ejercicio 3: Conectar el repositorio local a GitHub
Objetivo: Aprender a subir un proyecto a GitHub.
Pasos:
Entrar a GitHub y hacer clic en el botón ➕ ➜ New repository.


Nombrar el repo: mi_pagina_html, dejarlo público y NO marcar "Add a README".


Copiar la URL del repositorio (algo como https://github.com/tuusuario/mi_pagina_html.git).


En Git Bash, escribir:


git remote add origin https://github.com/tuusuario/mi_pagina_html.git
git branch -M main
git push -u origin main
Resultado esperado: El archivo index.html ahora está en GitHub.
========================================================
Ejercicio 4: Agregar un archivo CSS y subirlo
Objetivo: Añadir cambios y subirlos con Git.
Pasos:
Crear un archivo nuevo en la carpeta mi_pagina llamado style.css con este contenido:
body {
  background-color: lightblue;
}
2. Volver a Git Bash y escribir:
git add style.css
git commit -m "Agregué hoja de estilos"
git push
Resultado esperado: El archivo CSS aparece en GitHub.
===============================================
Ejercicio 5: Ignorar archivos con .gitignore
Objetivo: Aprender a excluir archivos del control de versiones.
Pasos:
Crear un archivo nuevo en la raíz llamado .gitignore.


Dentro del archivo, escribir:


*.log
config/
3. Crear un archivo llamado error.log y una carpeta config/ con un archivo config.txt dentro.


4. Escribir en Git Bash:
git status
Resultado esperado: Git ignora los archivos indicados.


=========================================================
Ejercicio 6: Clonar un repositorio de GitHub
Objetivo: Clonar un proyecto ajeno o compartido.
Pasos:
Buscar un repositorio público, por ejemplo: https://github.com/octocat/Hello-World


En Git Bash, escribir:
git clone https://github.com/octocat/Hello-World.git
Ingresar a la carpeta clonada y revisar su contenido.


Resultado esperado: Obtener una copia local del proyecto.
=========================================================
Ejercicio 7: Crear una nueva rama y hacer cambios
Objetivo: Usar ramas para experimentar sin afectar el código principal.
Pasos:
En el proyecto mi_pagina, escribir:
git checkout -b nueva_version
2. Modificar index.html para que diga:
<h1>¡Hola desde la nueva rama!</h1>


3. Guardar y ejecutar:
git add .
git commit -m "Modifiqué el saludo en nueva rama"
Volver a la rama principal:


git checkout main
Resultado esperado: Se puede cambiar entre versiones del proyecto.
=======================================================
Ejercicio 8: Unir ramas con merge
Objetivo: Fusionar el trabajo de dos ramas.
Pasos:
Desde la rama main, ejecutar:
git merge nueva_version
Resultado esperado: Los cambios de nueva_version ahora están en main.
==========================================================
Ejercicio 9: Recuperar un archivo borrado
Objetivo: Restaurar archivos con Git.
Pasos:
Borrar el archivo style.css desde Visual Studio.


En Git Bash, escribir:


git checkout HEAD style.css
Resultado esperado: ¡El archivo vuelve como por arte de magia!
=====================================================
Ejercicio 10: Documentar el proyecto con Markdown
Objetivo: Crear un archivo README.md.
Pasos:
Crear un archivo llamado README.md y escribir:
# Mi Página HTML
Este es mi primer proyecto usando Git y GitHub.
2. Luego en Git Bash:
git add README.md
git commit -m "Agregué documentación al proyecto"
git push
Resultado esperado: El proyecto ya está documentado.