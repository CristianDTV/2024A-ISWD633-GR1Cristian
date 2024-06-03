# Redes
Las redes son un componente fundamental que permite la comunicación entre contenedores, así como la comunicación de los contenedores con el mundo exterior. 
![Imagen](imagenes/redes.PNG)
- Bridge: Esta es la red por defecto en Docker. Permite la comunicación entre contenedores en el mismo host. Cada contenedor conectado a la red bridge tiene una IP propia en la subred de la red bridge.
    -  Brige por default: Cuando se ejecuta un contenedor, Docker crea automáticamente una red de tipo bridge por default. Esta red se utiliza para permitir la comunicación entre contenedores en el mismo host. Cada contenedor conectado a esta red obtiene su propia dirección IP en la subred de la red bridge.
    - Bridge creada por nosotros: Un usuario también puede crear sus propias redes de tipo bridge en Docker. Esto puede ser útil para organizar y segmentar los contenedores de una aplicación de manera más controlada. Al crear una red bridge personalizada, se puede especificar un rango de direcciones IP y otras configuraciones de red específicas. Los contenedores conectados a esta red utilizarán las direcciones IP de la subred definida por el usuario.
- Host: Con esta red, los contenedores comparten la red del host en lugar de tener su propia interfaz de red. Esto puede mejorar el rendimiento de red, pero los contenedores pueden entrar en conflicto con los puertos del host si intentan utilizar los mismos puertos.
- None: Con esta red, se deshabilita la configuración de red. Los contenedores que usan esta red tienen su propia red de bucle invertido y no pueden comunicarse con otros contenedores a menos que se conecten explícitamente a una red.

### Crear una red de tipo bridge

```
docker network create <nombre red> -d bridge
```
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/3fafa80e-a0c1-467b-b30e-41a7cdd698d0)

### Crear un contenedor vinculado a una red

```
docker run -d --name <nombre contenedor> --network <nombre red> <nombre imagen>
```
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/c264503e-6b6e-4f8e-8486-e7ce11bfc9ba)

### Para saber a qué red está conectado un contenedor

```
docker inspect <nombre contenedor>
```
ó
```
docker network inspect <nombre red> 
```
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/6e0a43ce-b12a-4755-9003-5c4da66598d0)

### Vincular contenedor a una red
```
docker network connect <nombre red> <nombre contenedor>
```
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/71be0ee9-9fb9-4128-b226-d4c8c746f8f0)

### Para desvincular un contenedor de una red
```
docker network disconnect <nombre red> <nombre contenedor>
```
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/2bd4d55d-688d-43fb-8ea3-2dc6ded93fca)

### Para listar las redes existentes
```
docker network ls
```
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/a207798d-1949-443a-b177-160c3c2bb884)

### Crear los contenedores y las redes que se presentan en el esquema. Usar para todos los contenedores la imagen de nginx:alpine

![Imagen](imagenes/esquema-ejercicio-redes.PNG)

# COLOCAR UNA CAPTURA DE LAS REDES EXISTENTES CREADAS
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/8e1577c2-702b-44ff-a0cb-0a5d26d58600)

# COLOCAR UNA(S) CAPTURAS(S) DE LOS CONTENEDORES CREADOS EN DONDE SE EVIDENCIE A QUÉ RED ESTÁN VINCULADOS
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/278a8b46-3997-47ca-b001-6272ecfb43b9)

# Eliminar las redes creadas
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/1c96f395-bf9b-4570-a332-1a24056ccf43)
