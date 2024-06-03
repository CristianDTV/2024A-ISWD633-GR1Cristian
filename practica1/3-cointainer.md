# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/2e765a90-65a4-4a40-9d04-aa700b2b6897)


Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/b39056b0-7f28-4224-99a2-cf78a072f021)


### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/393eea29-3a9c-40d9-b327-85bdc9633d46)


### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](imagenes/dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/6a773498-72ce-46ae-81e0-76eb27b11163)


**¿Qué sucede luego de la ejecución del comando?**
Al ejecutar este comando sin la opción -d, el contenedor se inicia en primer plano. Esto significa que mantendrá ocupada la línea de comandos hasta que el contenedor se detenga o se cierre manualmente.  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/933deec3-8cf2-4654-b672-8ef5ebfce2cd)


### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/3b968a15-4a3c-43c9-95ff-7c23044c7934)


Verificar que el contenedor que se eliminó

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/730926d8-3c5f-4d32-af05-bd132d6947d9)


### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/44686ce3-9ab6-4671-9bac-8f4291878440)


Verificar que el contenedor que se eliminó

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/020b8e30-7ee7-4d32-b83e-7254174fdbdf)

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/cfecd53d-ee89-46fb-83ea-115888bf3b3a)

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/1a02f47b-5556-4f0d-abf4-e42924bf0670)

