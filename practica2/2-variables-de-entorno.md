# Variables de Entorno
### ¿Qué son las variables de entorno
Las variables de entorno son especialmente útiles para configurar contenedores. Puedes pasar variables de entorno a un contenedor de Docker utilizando la opción -e o --env.

### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/2420ab97-33df-4664-9256-2c12569b205b)

### Crear un contenedor con mysql:8 , mapear todos los puertos

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/76102e36-ae76-4f20-a4f3-c1a59640a39a)

### ¿El contenedor se está ejecutando?
No

### Identificar el problema
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/99d01cac-9b46-4c4f-b897-4809c966290c)

### Eliminar el contenedor creado con mysql:8 
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/84bcb747-013a-46ee-843f-4f22361ac245)

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

Previo a esto es necesario crear el archivo y colocar las variables en un archivo, **.env** se ha convertido en una convención estándar, pero también es posible usar cualquier extensión como **.txt**.
```
docker run -d --name <nombre contenedor> --env-file=<nombreArchivo>.<extensión> <nombre imagen>
```
**Considerar**
Es necesario especificar la ruta absoluta del archivo si este se encuentra en una ubicación diferente a la que estás ejecutando el comando docker run.

### Crear un contenedor con mysql:8 , mapear todos los puertos y configurar las variables de entorno mediante un archivo
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/b72ba3b7-2bb0-4af7-b118-637a17d93315)

### ¿Qué bases de datos existen en el contenedor creado?
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/10e3aeb8-bf1d-49bf-aa94-4c69d2ff26a1)
