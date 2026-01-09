# Instalación y configuración inicial de Filezilla

## Instalación
Primero instalamos el servicio FTP en el sistema para que pueda aceptar conexiones. Los pasos son:
 1. Descargar FileZilla Server desde su web oficial.
 ![](https://github.com/JavierMoralesSimon/filezillaInstalacionYConfiguracion/blob/main/Capturas/1.1.png)
 2. Si el archivo descargado es el .deb, damos doble click en él y lo instalamos.
 ![](https://github.com/JavierMoralesSimon/filezillaInstalacionYConfiguracion/blob/main/Capturas/1.2.png)

## Consola de administración
Accedemos a la consola de administración la cual es una herramienta gráfica para administrar el servidor. Los pasos son:
 1. Abrir FileZilla Server Administration.
 2. Si nos pide conexión, dejamos el host y el puerto por defecto e introducimos una contraseña.
 ![](https://github.com/JavierMoralesSimon/filezillaInstalacionYConfiguracion/blob/main/Capturas/2.1.png)
 ![](https://github.com/JavierMoralesSimon/filezillaInstalacionYConfiguracion/blob/main/Capturas/2.2.png)

## Configuración
### Puerto de escucha:
Definir por qué puerto se conectarán los clientes FTP. Los pasos son:
 1. Ir a "Server - Configure".
 2. En "Server listeners - Port" ponemos el puerto 21 que es el típico.
 ![](https://github.com/JavierMoralesSimon/filezillaInstalacionYConfiguracion/blob/main/Capturas/3.1.png)

### Dirección IP:
Definir en qué interfaces de red aceptará conexiones el servidor. Esto se realiza en el mismo sitio que la configuración del puerto de escucha pero en el recuadro "Address". Ahí ponemos "0.0.0.0" para que escuche en todas las IPs. Una vez hechas estas dos primeras configuraciones, aplicamos cambios y aceptamos.
![](https://github.com/JavierMoralesSimon/filezillaInstalacionYConfiguracion/blob/main/Capturas/3.1.png)

### Inicio automático del servicio:
Hacer que el servidor arranque solo al iniciar Ubuntu mediante el comando `sudo systemctl enable filezilla-server`.
![](https://github.com/JavierMoralesSimon/filezillaInstalacionYConfiguracion/blob/main/Capturas/3.2.png)

### Reinicio del servidor
Reiniciar el servidor para que todos los cambios se apliquen mediante el comando `sudo systemctl restart filezilla-server`.
![](https://github.com/JavierMoralesSimon/filezillaInstalacionYConfiguracion/blob/main/Capturas/3.3.png)

## Servicio en funcionamiento
Comprobar que el servicio funciona mediante el comando `systemctl status filezilla-server`.
![](https://github.com/JavierMoralesSimon/filezillaInstalacionYConfiguracion/blob/main/Capturas/4.png)
