
# Nmap

`Nmap` es una herramienta de `escaneo de red` gratuita y de código abierto que se utiliza en pruebas de penetración (pentesting) para explorar y auditar redes y sistemas informáticos.

Con Nmap, los profesionales de seguridad pueden identificar los `hosts` conectados a una red, los `servicios` que se están ejecutando en ellos y las `vulnerabilidades` que podrían ser explotadas por un atacante. La herramienta es capaz de detectar una amplia gama de dispositivos, incluyendo enrutadores, servidores web, impresoras, cámaras IP, sistemas operativos y otros dispositivos conectados a una red.

Asimismo, esta herramienta posee una variedad de funciones y características avanzadas que permiten a los profesionales de seguridad adaptar la misma a sus necesidades específicas. Estas incluyen técnicas de escaneo agresivas, capacidades de scripting personalizadas, y un conjunto de herramientas auxiliares que pueden ser utilizadas para obtener información adicional sobre los hosts objetivo.

>> A la hora de escanear un puerto puede estar, `abierto`, `filtrado` (quiere decir que la herramenta no es capaz de determinar si el puerto esta abierto y que seguramente mediante un firewall se este protegiendo) o `cerrado`. 

>> Por detras para saber si esta abierto o cerrado opera cuando es escaneo TCP el `Tree Way Handshake` si esta abierto (SYN -> SYN/ACK -> ACK (established)), si esta cerrado (SYN -> RST(cerrado)). Tambien se puede hacer un escaneo por `UDP` pero por defecto nmap va por TCP.

>> Por el momento la idea es escanear los la ip, ver que puertos estan abiertos y luego escanear esos puertos

## Que es un firewall ?

Bueno, cuando escaneamos una ip vemos ciertos `puertos`, pero si logramos comprometer el equipo lo mas probable es que con los comandos `netstat` o `ss` veamos que hay mas puertos, bueno esto es porque hay un firewall "tapando" esos puertos y solo se ven internamente.
Tambien existen los IDS que son identificadores de intrusion (parecido a un firewall)
Basicamente es un sistema que esta hecho para detectar el acceso no autorizado y bloquearlo.

### Formas de evadir los firewall 

Cuando se realizan pruebas de penetración, uno de los mayores desafíos es evadir la detección de los Firewalls, que son diseñados para proteger las redes y sistemas de posibles amenazas. Para superar este obstáculo, Nmap ofrece una variedad de técnicas de evasión que permiten a los profesionales de seguridad realizar escaneos sigilosos y evitar así la detección de los mismos.

Algunos de los parámetros vistos en esta clase son los siguientes:

- MTU (–mtu): La técnica de evasión de MTU o “Maximum Transmission Unit” implica ajustar el tamaño de los paquetes que se envían para evitar la detección por parte del Firewall. Nmap permite configurar manualmente el tamaño máximo de los paquetes para garantizar que sean lo suficientemente pequeños para pasar por el Firewall sin ser detectados.

- Data Length (–data-length): Esta técnica se basa en ajustar la longitud de los datos enviados para que sean lo suficientemente cortos como para pasar por el Firewall sin ser detectados. Nmap permite a los usuarios configurar manualmente la longitud de los datos enviados para que sean lo suficientemente pequeños para evadir la detección del Firewall.

- Source Port (–source-port): Esta técnica consiste en configurar manualmente el número de puerto de origen de los paquetes enviados para evitar la detección por parte del Firewall. Nmap permite a los usuarios especificar manualmente un puerto de origen aleatorio o un puerto específico para evadir la detección del Firewall.

- Decoy (-D): Esta técnica de evasión en Nmap permite al usuario enviar paquetes falsos a la red para confundir a los sistemas de detección de intrusos y evitar la detección del Firewall. El comando -D permite al usuario enviar paquetes falsos junto con los paquetes reales de escaneo para ocultar su actividad.

- Fragmented (-f): Esta técnica se basa en fragmentar los paquetes enviados para que el Firewall no pueda reconocer el tráfico como un escaneo. La opción -f en Nmap permite fragmentar los paquetes y enviarlos por separado para evitar la detección del Firewall. Con el comando `-f` podemos fragmentar los paquetes enviados y asi por ahi el firewall no nos detecte y podamos leer si el puerto esta abierto o no, ya que por ahi el firewall espera que le mandemos un paquete de un tamanio especifico entonces al fragmentarlo no lo detectaria.

- Spoof-Mac (–spoof-mac): Esta técnica de evasión se basa en cambiar la dirección MAC del paquete para evitar la detección del Firewall. Nmap permite al usuario configurar manualmente la dirección MAC para evitar ser detectado por el Firewall.

- Stealth Scan (-sS): Esta técnica es una de las más utilizadas para realizar escaneos sigilosos y evitar la detección del Firewall. El comando -sS permite a los usuarios realizar un escaneo de tipo SYN sin establecer una conexión completa, lo que permite evitar la detección del Firewall.

- min-rate (–min-rate): Esta técnica permite al usuario controlar la velocidad de los paquetes enviados para evitar la detección del Firewall. El comando –min-rate permite al usuario reducir la velocidad de los paquetes enviados para evitar ser detectado por el Firewall.

Es importante destacar que, además de las técnicas de evasión mencionadas anteriormente, existen muchas otras opciones en Nmap que pueden ser utilizadas para realizar pruebas de penetración efectivas y evadir la detección del Firewall. Sin embargo, las técnicas que hemos mencionado son algunas de las más populares y ampliamente utilizadas por los profesionales de seguridad para superar los obstáculos que presentan los Firewalls en la realización de pruebas de penetración.






[Back](../introduccionHacking.md)