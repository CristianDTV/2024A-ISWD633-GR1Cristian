# Imagen
Es un archivo único que contiene todos los programas, librerías, dependencias y configuraciones necesarias para instalar y/o ejecutar una aplicación o un conjunto de aplicaciones.
![Imagen](imagenes/imagen.PNG)


## ¿Cuál es la relación entre una imagen y un contenedor? 
Una imagen de Docker es un archivo inmutable que contiene el código fuente, las bibliotecas, las dependencias, las herramientas y las configuraciones necesarias para ejecutar una aplicación. Es como una plantilla que define cómo se debe configurar y ejecutar un contenedor.

Un contenedor de Docker es una instancia en ejecución de una imagen. Cuando ejecutas una imagen, Docker crea un contenedor a partir de esa imagen. Los contenedores son aislados y tienen su propio sistema de archivos, red y entorno, pero pueden compartir el kernel del host y otras configuraciones según se necesite. En resumen, una imagen es el plano, y un contenedor es una construcción activa basada en ese plano.

![Imagen y contenedores](imagenes/imagenYcontenedores.JPG)
## Comandos para imágenes

### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/2d5f16f6-3bd3-4619-b15e-428e70ddaa40)


**¿Qué es nginx**
Nginx (pronunciado "engine-x") es un servidor web de código abierto y un servidor proxy inverso. 

Descargar la imagen  **nginx** en la versión **alpine**

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/656d7b23-1c7b-402e-9033-30b061a62d7c)


### Listar imágenes

```
docker images
```

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/70a875b8-227a-41a2-bc6a-3d05ab153027)


**Identificadores**
En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/a9fa69bb-74a7-4a61-bcbb-845bab88e68a)


**¿Con qué algoritmo se está generando el ID de la imagen**
Docker utiliza el algoritmo SHA-256 para generar el ID de la imagen. Este algoritmo produce un hash único para cada imagen, lo que garantiza que cada imagen pueda ser identificada de manera única y precisa.

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/adc72bfa-3d1c-4b60-befe-f2543c3377ab)


-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```

