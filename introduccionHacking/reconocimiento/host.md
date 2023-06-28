
# Reconocimiento de host

El descubrimiento de equipos en la red local es una tarea fundamental en la gestión de redes y en las pruebas de seguridad. Existen diferentes herramientas y técnicas para realizar esta tarea, que van desde el escaneo de puertos hasta el análisis de tráfico de red.

En esta clase, nos enfocaremos en las técnicas de descubrimiento de equipos basadas en los protocolos ARP e ICMP. Además, se presentarán diferentes herramientas que pueden ser útiles para esta tarea, como Nmap, netdiscover, arp-scan y masscan.

Entre los modos de escaneo que se explican en la clase, se encuentra el uso del parámetro ‘-sn‘ de Nmap, que permite realizar un escaneo de hosts sin realizar el escaneo de puertos. También se presentan las herramientas netdiscover, arp-scan y masscan, que utilizan el protocolo ARP para descubrir hosts en la red.

Cada herramienta tiene sus propias ventajas y limitaciones. Por ejemplo, netdiscover es una herramienta simple y fácil de usar, pero puede ser menos precisa que arp-scan o masscan. Por otro lado, arp-scan y masscan son herramientas más potentes, capaces de descubrir hosts más rápido y en redes más grandes, pero también son más complejas y pueden requerir más recursos.

En definitiva, el descubrimiento de equipos en la red local es una tarea fundamental para cualquier administrador de redes o profesional de seguridad de la información. Con las técnicas y herramientas adecuadas, es posible realizar esta tarea de manera efectiva y eficiente.

## Comandos 

- Nmap
```
nmap -sn 192.168.11.0/24 
```
	- Nmap tira por el protocolo ICMP esto quiere decir que hace ping a los host y prueba quien responde, sin ver los puertos, hace un escaneo de hosto (ya que aplicamos el '-sn'). Tambien tener en cuenta que savitar en este apartado explica que al hacer un escaneo para descubrir host englobemos un rango mas grande, yendonos a una subnetting de una clase mas arriba ej: 192.168.0.0/16 (tardara mas pero sera posible decubrir algun host 'oculto') Esto sucede porque el cliente crea otra subred pero piensa que la esta aislando y no es asi solo esta haciendo una subred 'una subnneting'.

- arp-scan
```
arp-scan -I <interface de red> --localnet
```

- netdiscover
```
netdiscover -i <interface de red>
```

- masscan 
```
masscan -p<puertos> -Pn 192.168.0.0/16 --rate=10000
```
	-Masscan es como nmap  pero mucho mas potente, nmap descubre miles de host por minutos mientras que masscan descubre millones de host por minuto, mientras nmap para cada puerto manda diferentes paquetes para descubrirlos de forma secuencial, masscan con un solo paquete puede descubrir que puertos estan abiertos para un unico host.



- Savitar muestra como hacer un script en bash para reconocer host, mediante traza ICMP que es lo que se explico antes de mandar ping a los host y ver quien responde. Puede pasar que los host no acepten pings entonces, lo que se hace es "atacar" los puertos mas comunes mediante tcp, todo esto en el script lo muestra.
