### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:11.21-alpine3.17
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/a5fd386f-fca6-40f4-b92e-02814524c82d)

### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/1e046ff7-91f7-4f72-9b32-57fe421157fb)


La figura presenta el esquema creado en donde los puertos son:
a: Puerto de pgAdmin4 en el host (80).
b: Puerto de pgAdmin4 en el contenedor (80).
c: No se expone el puerto de Postgres en el host (por lo tanto, no se asigna).

![Imagen](imagenes/esquema-ejercicio3.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/78f984e5-390b-4f4b-8054-e69c8e1b5b0c)
### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.

## Desde el servidor postgresl
### Acceder al servidor
### Conectarse a la base de datos info
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/45b08b8c-76bb-4dda-96e9-aff12193eff0)

### Realizar un select *from personas
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/bd7a4297-b53f-4ba2-8dec-f627d8779a05)
