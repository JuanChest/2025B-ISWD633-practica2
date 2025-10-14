### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:15-alpine3.21
# COMPLETAR
```
docker run -d --name postgresBD -e POSTGRES_PASSWORD=juanchest postgres:15-alpine3.21
```
### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4

# COMPLETAR
```
docker run --name postgres -e PGADMIN_DEFAULT_EMAIL=juan.cofre@epn.edu.ec -e PGADMIN_DEFAULT_PASSWORD=juanchest -p 80:80 dpage/pgadmin4
```

La figura presenta el esquema creado en donde los puertos son:
- a: 80
- b: 80
- c: 5432

![Imagen](esquema-2-ejercicio.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/0b90cedb-b409-41db-aafb-1632446406c2" />


# COMPLETAR CON UNA CAPTURA DEL LOGIN
### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.

## Desde el servidor postgresl
### Acceder al servidor
```
docker exec -it postgresBD bash
```
### Conectarse a la base de datos info
```
psql -h localhost -U postgres -d info
```
# COMPLETAR
### Realizar un select *from personas

<img width="377" height="161" alt="image" src="https://github.com/user-attachments/assets/2640e903-8e8b-400b-8627-f86618158ab0" />

# AGREGAR UNA CAPTURA DE PANTALLA DEL RESULTADO
