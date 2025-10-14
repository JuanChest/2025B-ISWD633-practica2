# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.

Consultar: Cómo se gestionan datos confidenciales con los secretos de Docker (Docker Secrets).

Los datos secretos o confidenciales se gestionan con los secretos de Docker mediante el cifrado, con esto se entrega la información de forma segura y se la entrega solamente a los contenedores autorizados.

Docker Swarm
- Los secretos se crean y se gestionan en un Docker Swarm
- Los secretos se crean en el nodo manager del swarm con:
```
docker secret create <nombre> <archivo>
```
- Los secretos se cifran y distribuyen a los nodos del swarm, y solo los contenedores autorizados pueden acceder a ellos

Docker Compose
- Se define un secreto con el nombre del archivo que lo contiene
```
docker-compose.yml
```
- Al ejecutar ```docker compose up```, Compose automáticamente monta el secreto como un archivo en la ruta ```/run/secrets/mi_secreto_key``` dentro del contenedor.
- La aplicación dentro del contenedor debe estar configurada para leer la información confidencial desde esa ruta específica en el sistema de archivos.
