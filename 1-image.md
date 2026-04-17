# Imagen
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
<img width="813" height="205" alt="image" src="https://github.com/user-attachments/assets/909c004c-e0c1-483f-b15c-b74362725d04" />

# COMPLETAR

**¿Qué es nginx?**

Nginx es un software de servidor web que también funciona como proxy inverso y balanceador de carga, encargado de recibir las solicitudes de los usuarios y responder entregando contenido web o redirigiéndolas a otros servidores; se utiliza para servir páginas, distribuir tráfico y mejorar el rendimiento de aplicaciones, destacándose por su alta eficiencia y capacidad de manejar miles de conexiones simultáneas con bajo consumo de recursos.

# COMPLETAR 

Descargar la imagen  **nginx** en la versión **alpine**

docker pull nginx:alpine

# COMPLETAR

### Listar imágenes

```
docker images
```

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 

<img width="762" height="87" alt="image" src="https://github.com/user-attachments/assets/0c8a2507-734f-4edf-8b63-4e17147f605e" />

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 

<img width="762" height="581" alt="image" src="https://github.com/user-attachments/assets/57d63e29-d94a-469a-81d4-56e6080d2c5a" />

# COMPLETAR

**¿Con qué algoritmo se está generando el ID de la imagen**

El ID de una imagen se genera mediante un algoritmo de hash criptográfico llamado SHA-256, el cual toma el contenido de la imagen (como sus capas y configuración) y produce un identificador único.

# COMPLETAR

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
# COMPLETAR

-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
