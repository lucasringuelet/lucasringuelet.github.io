---
layout: default
---

# Que es un protocolo?
> Un protocolo de red define el `formato` y el `orden` de los mensajes intercambiados entre
> dos o mas entidades.
>
> Por ejemplo se puede hacer una analogia humana: 
> Los humanos para comunicarse o para mantener una conversacion tienen ciertas "reglas" del
> lenguaje, ejemplo: Cuando decis "hola" lo mas probable es que la otra persona te responda
> "hola", no creo que te responda de la nada la palabra "auto", pero si te puede responder 
> "chau" o directamente no responderte y "se terminaria la conversacion/coneccion".
> Bueno eso es un protocolo, unas reglas ya dadas para cada situacion o conversacion que
> se quiera plantear.
>
> Esto mismo sucede con las computadoras, lo unico que para esas ditintas conversaciones o 
> situaciones se usan ditintos protocolos; Existen muchos pero los mas comunes son el tcp/ip

## Protocolo tcp(Transmission Control Protocol)/ip(internet protocol):
> El protocolo tcp te asegura que la informacion va a llegar tal y como esta del origen al 
> destino. Y utiliza el 'Tree-Way Handshake':
>> ### Tree-Way Handshake
	A la hora de entablar una coneccion con tcp se suele ver ( SYN -> SYN ACK -> ACK)
	es como se entabla la coneccion ( en 3 pasos de ahi el nombre )
	
![tree](https://www.techopedia.com/wp-content/uploads/2023/03/ad900dc1-ad94-4c7b-a3f8-154ad27c35f1.png)

> El protocolo ip es el encargado de determinar la ruta por donde iran esos paquetes.
>
> TCP descompone la informacion en paquetes y los reenvia a la capa del protocolo IP

## Protocolo udp(User Datagram Protocol)
> UDP es un tambien un protocolo para enviar paquetes de informacion, pero este, no asegura
> llegue exitosamente al destinataraio o que no se corrompa en el camino. Entonces para que 
> utilizariamos udp en lugar de tcp, bueno porque la diferencia radica en la velocidad, udp
> es mas rapido que tcp. Entonces por ejemplo udp lo podemos utilizar para las video llamadas
> ya que necesitamos una coneccion instantanea y si se pierde algun paquete o se corrompe en 
> el camino sera minimo.
> Tambien se ahorra tiempo porque este protocolo no requiere que se establesca una coneccion
> formal con el destinatario (por ejemplo el handshake del tcp), udp simplemente pide la
> informacion y un equipo se la empieza a dar, gracias a esto se ahorra tiempo. Por eso 
> UDP es recomendable en programas que requieran mas velocidad que fiabilidad a la hora de 
> enviar los paquetes.

### Puertos tcp comunes
`Puerto` 0: TCP en realidad no usa el puerto 0 para la comunicación de red, pero este puerto es bien conocido por los programadores de redes. Los programas de socket TCP usan el puerto 0 por convención para solicitar que el sistema operativo elija y asigne un puerto disponible. Esto evita que un programador tenga que elegir («codificar») un número de puerto que podría no funcionar bien para la situación.

`Puerto` 21: El puerto 21 por norma general se usa para las conexiones a servidores FTP en su canal de control, siempre que no hayamos cambiado el puerto de escucha de nuestro servidor FTP o FTPES.

`Puerto` 22: Por normal general este puerto se usa para conexiones seguras SSH y SFTP, siempre que no hayamos cambiado el puerto de escucha de nuestro servidor SSH.

`Puerto` 23: Telnet, sirve para establecer conexión remotamente con otro equipo por la línea de comandos y controlarlo. Es un protocolo no seguro ya que la autenticación y todo el tráfico de datos se envía sin cifrar.

`Puerto` 25:  El puerto 25 es usado por el protocolo SMTP para él envió de correos electrónicos, también el mismo protocolo puede usar los puertos 26 y 2525.

`Puerto` 53: Es usado por el servicio de DNS, Domain Name System.

`Puerto` 80: Este puerto es el que se usa para la navegación web de forma no segura HTTP.

`Puerto` 101: Este puerto es usado por el servicio Hostname y sirve para identificar el nombre de los equipos.

`Puerto` 110: Este puerto lo usan los gestores de correo electrónico para establecer conexión con el protocolo POP3.

`Puerto` 123: Es un puerto utilizado por el NTP o Protocolo de tiempo en red, es uno de los protocolos más importantes a nivel de redes, ya que se utiliza para mantener los dispositivos sincronizados en Internet. Podemos incluso considerarlo vital, ya que, debido a la precisión de los relojes, facilitan mucho la interrelación de problemas de un dispositivo a otro.

`Puertos` 137, 138 y 139: Estos puertos son utilizados por el Protocolo NetBIOS o NBT, lo habréis escuchado mucho si trabajáis en redes en Windows, ya que ha sido durante mucho tiempo el protocolo TCP principal para interconectar los equipos que están bajo este sistema operativo, lógicamente se utiliza en la mayoría de las veces en combinación con el IP utilizando así la famosa combinación TCP/IP que todos conocemos en este mundillo.

`Puerto` 143: El puerto 143 lo usa el protocolo IMAP que es también usado por los gestores de correo electrónico.

`Puerto` 179: Es el puerto utilizado por el Protocolo de puerta de enlace fronteriza o BGP por sus siglas en inglés, es otro protocolo muy importante a nivel de redes, ya que, en su mayoría, es utilizado por los proveedores de servicio para ayudar a mantener las enormes tablas de enrutamiento que existen hoy en día. También es utilizado para procesar las inmensas cantidades de tráfico en las redes, por lo que es uno de los protocolos más utilizados en las redes públicas.

`Puerto` 194: Aunque herramientas como aplicaciones de mensajería para teléfonos inteligentes y servicios como Slack y Microsoft Teams han reducido el uso de Internet Relay Chat, IRC sigue siendo popular entre personas de todo el mundo. Por defecto, IRC usa el puerto 194.

`Puerto` 443: Este puerto es también para la navegación web, pero en este caso usa el protocolo HTTPS que es seguro y utiliza el protocolo TLS por debajo.

`Puerto` 445: Este puerto es compartido por varios servicios, entre el más importante es el Active Directory.

`Puerto` 587: Este puerto lo usa el protocolo SMTP SSL y, al igual que el puerto anterior sirve para el envío de correos electrónicos, pero en este caso de forma segura.

`Puerto` 591: Es usado por Filemaker en alternativa al puerto 80 HTTP.

`Puerto` 853: Es utilizado por DNS over TLS.

`Puerto` 990: Si utilizamos FTPS (FTP Implícito) utilizaremos el puerto por defecto 990, aunque se puede cambiar.

`Puerto` 993: El puerto 993 lo usa el protocolo IMAP SSL que es también usado por los gestores de correo electrónico para establecer la conexión de forma segura.

`Puerto` 995: Al igual que el anterior puerto, sirve para que los gestores de correo electrónico establezcan conexión segura con el protocolo POP3 SSL.

`Puerto` 1194: Este puerto está tanto en TCP como en UDP, es utilizado por el popular protocolo OpenVPN para las redes privadas virtuales.

`Puerto` 1723: Es usado por el protocolo de VPN PPTP.

`Puerto` 1812: se utiliza tanto con TCP como con UDP, y sirve para autenticar clientes en un servidor RADIUS.

`Puerto` 1813: se utiliza tanto con TCP como con UDP, y sirve para el accounting en un servidor RADIUS.

`Puerto` 2049: es utilizado por el protocolo NFS para el intercambio de ficheros en red local o en Internet.

`Puertos` 2082 y 2083: es utilizado por el popular CMS cPanel para la gestión de servidores y servicios, dependiendo de si se usa HTTP o HTTPS, se utiliza uno u otro.

`Puerto` 3074: Lo usa el servicio online de videojuegos de Microsoft Xbox Live.

`Puerto` 3306: Puerto usado por las bases de datos MySQL.

`Puerto` 3389: Es el puerto que usa el escritorio remoto de Windows, muy recomendable cambiarlo.

`Puerto` 4662 TCP y 4672 UDP: Estos puertos los usa el mítico programa eMule, que es un programa para descargar todo tipo de archivos.

`Puerto` 4899: Este puerto lo usa Radmin, que es un programa para controlar remotamente equipos.

`Puerto` 5000: es el puerto de control del popular protocolo UPnP, y que por defecto, siempre deberíamos desactivarlo en el router para no tener ningún problema de seguridad.

`Puertos` 5400, 5500, 5600, 5700, 5800 y 5900: Son usados por el programa VNC, que también sirve para controlar equipos remotamente.

`Puertos` 6881 y 6969: Son usados por el programa BitTorrent, que sirve para e intercambio de ficheros.

`Puerto` 8080: es el puerto alternativo al puerto 80 TCP para servidores web, normalmente se utiliza este puerto en pruebas.

`Puertos` 51400: Es el puerto utilizado de manera predeterminada por el programa Transmission para descargar archivos a través de la red BitTorrent.

`Puerto` 25565: Puerto usado por el famoso videojuego Minecraft.
### ATENCION
	Un aspecto muy importante de los puertos TCP, es que existe un rango de puertos desde el 49152 al 65535 que son los puertos efímeros, es decir, con cada conexión de origen que nosotros realicemos, se utilizan estos puertos que son dinámicos. Por ejemplo, si realizamos una petición a una web, el puerto de origen estará en este rango 49152-65535, y el puerto de destino será el 80 (HTTP) o 443 (HTTPS).



### Puertos udp comunes
`Puerto` 23: Este puerto es usado en dispositivos Apple para su servicio de Facetime.

`Puerto` 53: Es utilizado para servicios DNS, este protocolo permite utilizar tanto TCP como UDP para la comunicación con los servidores DNS.

`Puerto` 67: Los servidores del Protocolo de configuración dinámica de host usan el puerto UDP 67 para escuchar las solicitudes.

`Puerto` 68: Por su parte los clientes DHCP se comunican en el puerto UDP 68.

`Puerto` 69: Este puerto es utilizado sobre todo por el Protocolo trivial de transferencia de archivos o TFTP, dicho protocolo es el que nos ofrece un método para transferir nuestros archivos, pero sin tantos requisitos para el establecimiento de sesiones como podría por ejemplo utilizar el FTP. Cabe destacar que al utilizar UDP en lugar de TCP, este protocolo no puede garantizar de ninguna forma que nuestros archivos hayan sido transferidos de manera correcta, por lo que el dispositivo al que lo estamos enviando, debe tener la capacidad de verificar que dicha transferencia se ha realizado adecuadamente.

`Puerto` 88: El servicio de juegos en red de Xbox utiliza varios números de puerto diferentes, incluido el puerto UDP 88.

`Puerto` 161: De manera predeterminada, el Protocolo simple de administración de redes usa el puerto UDP 161 para enviar y recibir solicitudes en la red que se administra.

`Puerto` 162: Se utiliza el puerto UDP 162 como predeterminado para recibir capturas SNMP desde dispositivos administrados.

`Puerto` 500: este puerto es utilizado por el protocolo de VPN IPsec, concretamente se usa por ISAKMP para la fase 1 del establecimiento de la conexión con IPsec.

`Puerto` 514: Es usado por Syslog, el log del sistema operativo.

`Puerto` 1194: este puerto es el predeterminado del protocolo OpenVPN, aunque también se puede utilizar el protocolo TCP. Lo más normal es usar UDP 1194 porque es más rápido a la hora de conectarnos y también de transferencia, obtendremos más ancho de banda.

`Puerto` 1701: Es usado por el protocolo de VPN L2TP.

`Puerto` 1812: se utiliza tanto con TCP como con UDP, y sirve para autenticar clientes en un servidor RADIUS.

`Puerto` 1813: se utiliza tanto con TCP como con UDP, y sirve para el accounting en un servidor RADIUS.

`Puerto` 4500: este puerto también es utilizado por el protocolo de VPN IPsec, se utiliza este puerto para que el funcionamiento de la NAT sea perfecto. Este puerto se utiliza en la fase 2 del establecimiento IPsec, pero también tenemos que tener abierto el puerto UDP 500.

`Puerto` 51871: es utilizado por el protocolo de VPN Wireguard de manera predeterminada.


### Puertos mas utilizados
>Como puedes ver, existen gran cantidad de puertos en Internet que se utilizan para las diferentes aplicaciones y servicios que nos podemos encontrar y utilizar. Cada uno de ellos tiene su función específica en la transmisión de datos. Pero hay algunos de ellos, los cuales tienen un índice de uso mucho más alto que los demás, lo cual los convierte en los más utilizados. Estos son:

`Puerto` 80: Es el puerto utilizado por HTTP, el protocolo de transferencia de hipertexto que se utiliza para acceder a todas las páginas web. La mayoría de los sitios web lo utilizan para transmitir todo su contenido.

`Puerto` 443: Es el puerto utilizado por HTTPS, el protocolo de transferencia de hipertexto seguro. Permite la transmisión segura de datos por toda la red y se utiliza para transacciones en línea, como compras, transacciones bancarias, bolsa, entre otros.

`Puerto` 21: Es el puerto utilizado por el protocolo FTP (File Transfer Protocol), que se utiliza para la transferencia de archivos entre dispositivos en una red. Su uso principal es para la transferencia de archivos grandes, como imágenes o videos entre otros archivos.

`Puerto` 22: Es el puerto utilizado por el protocolo SSH (Secure Shell), que se utiliza para la conexión segura a un servidor remoto. Es utilizado por los administradores de sistemas para la gestión de servidores, entre otras aplicaciones con funciones similares.

`Puerto` 25: Es el puerto utilizado por el protocolo SMTP (Simple Mail Transfer Protocol), que se utiliza para la transferencia de correo electrónico. Se utiliza para poder enviar correos electrónicos desde un cliente de correo electrónico a un servidor de correo electrónico.

`Puerto` 53: Es el puerto utilizado por el protocolo DNS (Domain Name System), que se utiliza para traducir nombres de dominio en direcciones IP. Es esencial para la navegación por internet hoy en día, ya que permite que los navegadores web accedan a los sitios web utilizando nombres de dominio y no direcciones IP que son más complicadas.

`Puerto` 110: Es el puerto utilizado por el protocolo POP3 (Post Office Protocol version 3), que se utiliza para recibir correo electrónico en un cliente de correo electrónico. En combinación con el puerto 25.

[Back](../introduccionHacking.md)