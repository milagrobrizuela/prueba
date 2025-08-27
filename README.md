# PASOS PARA CLONAR UN REPOSITORIO Y CREAR UNA RAMA

1. Clonar tu repositorio
    Abrí Git Bash en la carpeta donde quieras tener el proyecto y ejecutá:
    git clone https://github.com/milagrobrizuela/prueba.git
    Esto crea una carpeta llamada prueba con tu repo dentro.

2. Entrar a la carpeta del repo
    cd prueba

3. Crear una nueva rama (ejemplo: mi-rama)
    git switch -c mi-rama

4. Verificar en qué rama estás
    git branch
    Te va a mostrar todas las ramas. La que tenga * es la activa.

5. Subir la nueva rama a GitHub
    Cuando quieras publicar tu rama en remoto:
    git push -u origin mi-rama

6. Ir a la rama principal
    Primero asegurate de estar en main (la rama que va a recibir los cambios:
    git switch main

7. Traer los últimos cambios de GitHub (opcional pero recomendable)
    git pull origin main
    Esto asegura que tu main local esté actualizado antes del merge.

8. Hacer el merge de tu rama
    git merge mi-rama
    Git intentará integrar los cambios automáticamente.
    Si hay conflictos (dos cambios en la misma línea de un archivo), Git te avisará y tendrás que resolverlos manualmente antes de continuar.

9. Subir los cambios a GitHub
    git push origin main
    Ahora tu main en GitHub tendrá los cambios que tenías en mi-rama.

10. Después de un merge exitoso, normalmente borrás la rama
    Primero asegurate de no estar en esa rama:
    git switch main  # volvés a main
    git branch -d mi-rama  # borra la rama si ya hiciste merge
    git branch -D mi-rama  # fuerza borrar aunque no hayas hecho merge