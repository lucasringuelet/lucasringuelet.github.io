
# Modelo OSI

El modelo `OSI` no es mas que un estandar conceptual para agrupar los ditintos protocolos en diferentes capas. Se utiliza para justamente estandarizar y que todos "hablemos el mismo idioma".

Ayuda a definir de forma organizada y estructurada el proceso de comunicacion entre redes de ordenadores, mediante la utilizacion de capas(donde en esas capas estaran los distintos protocolos).

## Tipos de capas
	
	Para explicar las distintas capas utilizaremos una semejanza con el envio de un paquete por correo.


1. Fisica
	> Serian las calles por donde viajan los paquetes, son los cables por donde se transmiten estos paquetes para que lleguen a la siguiente capa.

1. Enlace de Datos
	> Seria el inspector que verifica que este el paquete correctamente, que no tenga ningun defecto y controla el flujo con el que se envian los paquetes, esta capa recibe los paquetes de la capafisica y si tienen algun problema ver si se pueden corregir, de esta forma las capas superiores pueden asegurarse que los paquetes que le llegaran estaran bien, ya que esta capa se encarga de eso.

1. Red
	> En esta capa se puede decir que es la oficina de correos, cuando enviamos un correo la oficina determina quien es el destinatario y quien es el remitente, en caso de que hayan demasiados mensajes para enviar pueden llegar a priorizar cuales se enviaran primero y tambien determinaran cual es la mejor forma de enviar esa carta. Esta es la capa mas activa en internet ya que aqui es donde tenemos el direccionamiento IP de origen y destino, y tambien como dijimos antes pueden priorizar paquetes sobre otros y cual es el mejor camino para enviar el paquete hacia esa direccion IP.

1. Transporte
	> Camiones y carteros, en esta capa es donde se garantiza que los paquetes lleguen en perfecto estado.
	Justamente los protocolos que actuan en esta capa son los TCP y UDP.

1. Sesion
	> Esta capa se encarga de establecer y mantener las sesiones de comunicacion entre los dispositivos. Tambien te proporciona servicios de gestion de sesiones, como la autenticacion y la autorizacion.

1. Presentacion
	> Esta capa se encarga de la representacion de datos, proporcionando funciones como la codificacion y decodificacion de datos, la compresion y el cifrado para presentarsela a la capa siguiente.

1. Aplicacion
	> Es la capa para consumir los datos, como correo electronico, navegadores web y transferencia de archivos. Basicamente proporciona servicios para aplicaciones de usuario finales. Aqui es donde estan los protocolos http, ftp, etc.


[Back](../introduccionHacking.md)