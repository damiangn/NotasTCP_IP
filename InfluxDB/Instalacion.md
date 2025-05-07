# Pasos para instalar influxDB 2.0 en Linux Debian

1- Primero se crea un directorio:	
```bash
mkdir -p ~/influxdb2/data ~/influxdb2/config
```

2- Iniciamos un docker con la imagen de influxDB, si no se tiene, la descargará y después creará el contenedor
con esa imagen:

```bash
docker run -d \                                                                                                11:06:19 
  --name influxdb \
  -p 8086:8086 \
  -v ~/influxdb2/data:/var/lib/influxdb2 \
  -v ~/influxdb2/config:/etc/influxdb2 \
  influxdb:2
```

3- Para ver si está corriendo ponemos
```bash
docker ps -a
```

4- Entramos al navegador Web y nos dirigimos al localhost, puerto 8086. Nos tenemos que crear un nombre de usuario,
contraseña, nombre de organización y un nombre de bucket, que es para crear una tabla con el nombre de la
categoría que elijamos, por ejemplo sensores en nuestro caso que estamos trabajando con los ESP32 y ESP8266.

 
