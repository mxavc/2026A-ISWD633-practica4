# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.

Conocimientos antes de la práctica
Tenía nociones generales de cómo construir imágenes con Docker, pero no comprendía en detalle:
-Cómo cada instrucción del Dockerfile se traduce en una capa independiente.
-La importancia de usar CMD en primer plano (apachectl -D FOREGROUND) para que Docker pueda monitorear el proceso.
-Las dificultades que surgen al trabajar con imágenes antiguas como CentOS 7 (repositorios obsoletos).

Conocimientos después de la práctica
-Aprendí a automatizar la instalación de Apache y la copia de archivos web mediante un Dockerfile.
-Comprendí que cada instrucción (FROM, RUN, COPY, EXPOSE, CMD) genera una capa que puede ser reutilizada en futuras construcciones.
-Identifiqué que el mecanismo de caché permite que, al modificar solo index.html, Docker reutilice las capas anteriores y reconstruya únicamente la capa afectada.
-Reconocí la importancia de usar imágenes base actualizadas (Rocky Linux, AlmaLinux) para evitar problemas de repositorios.
-Entendí cómo mapear puertos (-p o -P) y verificar el puerto host asignado con docker ps.

Problemas solucionados
Error con repositorios de CentOS 7:  
Al ejecutar yum update, los repositorios oficiales ya no estaban disponibles.
Solución: usar una imagen más reciente como Rocky Linux.