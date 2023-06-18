
# Sockets y Puertos
A menudo se suele confundir un socket TCP o UDP con los puertos TCP o UDP. Un socket, como hemos dicho antes, está formado por el protocolo de la capa de transporte, la dirección IP de origen y destino, así como los puertos de origen y destino. Los «puertos» solamente es una parte del socket, una parte fundamental pero solamente una parte, para poder formar un socket es necesario contar también con las correspondientes direcciones IP para que pueda haber comunicación punto a punto entre dos procesos.

Cuando nosotros abrimos un puerto en el router, realmente lo que estamos haciendo es permitir una comunicación desde el exterior (Internet) hacia dentro de la red local, atravesando la NAT que todos los routers tienen para el protocolo IPv4. Cuando estamos en un entorno NAT, el router se encargará de traducir las direcciones IP privadas en la pública, con el objetivo de poder enrutar correctamente todo el tráfico a Internet.

En el caso de que cualquier cliente dentro de la NAT desee comunicarse con un servidor web que está en Internet, el socket que creará este cliente local será algo como esto:

>Protocolo: TCP.
 >IP origen: 192.168.1.2 (nosotros).
 >IP destino: 88.88.88.88 (el servidor web).
 >Puerto origen o local: 49152 (nosotros).
 >Puerto destino o remoto: 443 (servidor web).

Entonces el router cogerá esta conexión, y la traducirá en lo siguiente, para que pueda ser enrutada a través de Internet, creando un nuevo socket entre el router y el servidor web remoto:

>Protocolo: TCP.
 >IP origen: 20.20.20.20 (nuestra IP pública).
 >IP destino: 88.88.88.88 (el servidor web).
 >Puerto origen o local: 49152 (nosotros).
 >Puerto destino o remoto: 443 (servidor web).

En el caso de que la comunicación sea al revés (desde fuera de la NAT hacia dentro de la NAT), es cuando debemos abrir un puerto en nuestro router para que se pueda alcanzar el servidor desde el exterior, de lo contrario, el firewall del router parará toda comunicación.

[Back](../introduccionHacking.md)