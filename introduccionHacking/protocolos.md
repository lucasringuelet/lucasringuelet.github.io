---
layout: default
---

# Que es un protocolo?
> Un protocolo de red define el 'formato' y el 'orden' de los mensajes intercambiados entre
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



[Back](../introduccionHacking.md)