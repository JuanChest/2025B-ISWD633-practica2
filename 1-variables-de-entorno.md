# Variables de Entorno
### ¿Qué son las variables de entorno?

Es una variable dinámica del sistema operativo que permite almacenar información de configuración de aplicaciones.

# COMPLETAR

### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

```
docker run -d --name nginx -e username=JuanChest -e rol=admin nginx:alpine
```
```
docker inspect nginx
```
<img width="1210" height="333" alt="image" src="https://github.com/user-attachments/assets/a5cf874c-af1e-4d2b-95fc-42827ba3f04a" />

# COMPLETAR
# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR

### Crear un contenedor con la imagen de mysql, mapear todos los puertos
# COMPLETAR

```
docker run -d -P --name mysql mysql:latest
```

### ¿El contenedor se está ejecutando?
# COMPLETAR

No
### Identificar el problema

La base de datos no esta inicializada y además hay variables de entorno no configuradas.

    - MYSQL_ROOT_PASSWORD
    
    - MYSQL_ALLOW_EMPTY_PASSWORD
    
    - MYSQL_RANDOM_ROOT_PASSWORD

    
# COMPLETAR

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

### Crear un contenedor con mysql, mapear todos los puertos y configurar las variables de entorno mediante un archivo
```
docker run -d -P --name some-mysql -e MYSQL_ROOT_PASSWORD=holadios -d mysql:latest
```

<img width="1155" height="791" alt="image" src="https://github.com/user-attachments/assets/4803e683-d641-444c-b488-5369fd08c91d" />


# COMPLETAR

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR 

### ¿Qué bases de datos existen en el contenedor creado?

+--------------------+

| Database           |

+--------------------+

| information_schema |

| mysql              |

| performance_schema |

| sys                |

+--------------------+
# COMPLETAR
