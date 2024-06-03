# VOLUMEN TIPO HOST
Un volumen host (o bind mount) es un tipo de volumen donde se monta un directorio o archivo específico del sistema de archivos del host en un contenedor.

```
docker run -d --name <nombre contenedor> -v <ruta carpeta host>:<ruta carpeta contenedor> <imagen> 
```

### Crear un volumen tipo host con la imagen nginx:alpine, para la ruta carpeta host: directorio en donde se encuentra la carpeta html en tu computador y para la ruta carpeta contenedor: /usr/share/nginx/html esta ruta se obtiene al revisar la se obtiene desde la documentación
![Volúmenes](imagenes/volumen-host.PNG)
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/d17b991c-2d3a-47a7-a148-c3893ca9643a)


### ¿Qué sucede al ingresar al servidor de nginx?
Al ingresar al servidor de nginx, se verá el contenido del directorio montado desde el host. Esto significa que cualquier archivo HTML o recursos estáticos (CSS, JS, imágenes) en la carpeta html del host serán servidos por nginx.

### ¿Qué pasa con el archivo index.html del contenedor?
El archivo index.html del contenedor será reemplazado por el index.html del directorio montado desde el host. Si el directorio del host no contiene un archivo index.html, nginx mostrará un error 403 (Forbidden) o 404 (Not Found), dependiendo de la configuración.

### Ir a https://html5up.net/ y descargar un template gratuito, descomprirlo dentro de nginx/html
### ¿Qué sucede al ingresar al servidor de nginx?
Al ingresar al servidor de nginx, se verá el nuevo template HTML que has descargado y descomprimido en la carpeta html del host. Nginx servirá este contenido actualizado.

### Eliminar el contenedor
![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/e96dbffc-ec07-4723-a5a3-7297b5b600d4)

### ¿Qué sucede al crear nuevamente el mismo contenedor con volumen de tipo host a los directorios definidos anteriormente?
Al crear nuevamente el mismo contenedor con el volumen de tipo host a los mismos directorios definidos, el contenido del contenedor nginx será el mismo que el contenido del directorio del host. Esto significa que nginx servirá el contenido actualizado del directorio html del host.

### ¿Qué hace el comando pwd?
El comando pwd (print working directory) muestra la ruta completa del directorio actual en el que te encuentras. En el contexto de Docker, se puede usar para obtener la ruta actual de trabajo y montar directorios correctamente.

![image](https://github.com/CristianDTV/2024A-ISWD633-GR1Cristian/assets/158982181/766183ef-43c1-4fc9-95aa-cc1577c7bebd)

### Volumen tipo host usando PWD y PowerShell
```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v ${PWD}/<ruta relativa>:<ruta absoluta> <nombre imagen>:<tag> 
```

### Volumen tipo host usando PWD (Git Bash)

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v $(pwd -W)/html:/usr/share/nginx/html <nombre imagen>:<tag> 
```

### Volumen tipo host usando PWD (en Linux)

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v $(pwd)/html:/usr/share/nginx/html <nombre imagen>:<tag> 
```

