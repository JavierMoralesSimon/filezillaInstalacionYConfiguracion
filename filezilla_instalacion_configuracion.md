# Instalación y configuración inicial de Filezilla

## Instalación
Primero instalamos el servicio FTP en el sistema para que pueda aceptar conexiones. Los pasos son:
 1. Descargar FileZilla Server desde su web oficial.
 2. Si el archivo descargado es el .deb, damos doble click en él y lo instalamos.

## Consola de administración
Accedemos a la consola de administración la cual es una herramienta gráfica para administrar el servidor. Los pasos son:
 1. Abrir FileZilla Server Administration.
 2. Si nos pide conexión, dejamos el host y el puerto por defecto e introducimos una contraseña.

## Configuración
  * Puerto de escucha:
    Definir por qué puerto se conectarán los clientes FTP. Los pasos son:
     * Ir a "Server - Configure".
     * En "Server listeners - Port" ponemos el puerto 21 que es el típico.
  * Dirección IP:
    Definir en qué interfaces de red aceptará conexiones el servidor. Esto se realiza en el mismo sitio que la configuración del puerto de escucha pero en el recuadro Address. Ahí ponemos "0.0.0.0" para que escuche en todas las IPs. Una vez hecho estas dos primeras configuraciones, aplicamos cambios y aceptamos.
  * Inicio automático del servicio:
    Hacer que el servidor arranque solo al iniciar Ubuntu mediante el comando `sudo systemctl enable filezilla-server`.
Reiniciar el servidor para que todos los cambios se apliquen mediante el comando `sudo systemctl restart filezilla-server`.

## Servicio en funcionamiento
Comprobar que el servicio funciona mediante el comando `systemctl status filezilla-server`.
