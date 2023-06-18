
# Subnetting

 -- Que es el subnetting ?

 	El subnetting es una tecnica utilizada para dividir una red IP en subredes mas chicas y manejables. Esto se logra mediante el uso de mascaras de red, que permiten definir que bits de la direccion IP corresponden a la red y cuales a los host.

 	Gracias a esto nosotros como atacantes podemos al ver una direccion MAC darnos cuenta como esta estructurada la red a atacar, y ver de que forma proceder a la hora de escanear.

 -- Mascara de red

 	Por ejemplo una mascara de red 255.255.255.0 indica que los primeros tres octetos de la direccion IP corresponden a la red, mientras que el ultimo octeto se utiliza para los host.

 -- CIDR (acronimo de `Classless Inter-Domain Routing`)

 	Cuando hablamos de cidr, a lo que hacemos referencia es a un metodo de asignacion de direcciones IP mas eficiente y flexible que el uso de clases de redes IP fijas. Con CIDR, una direccion IP se representa mediante una direccion IP base y una mascara de red, que se escriben juntas separadas por una barra (/).

 	Por ejemplo, la direccion IP 192.168.1.1 con una mascara de red de 255.255.255.0 se escribiria como 192.168.1.1/24.

 	La mascara de red se representa en notacion prefijo, que indica el numero de its que estan en `1` en la mascara. En este caso, la mascara de red 255.255.255.0 tiene 24 bits en `1` (los primeros tres octetos), por lo qye su notacion de prefijo es /24.


 > Se puede entrar mas en detalle y sacar toda la subred que este en una direccion ip a  mano calculando y >teniendo en cuenta los bits, pero por mas que este bien saberlo como se hace y que sucede por detras hay >paginas web que dadas una direccion ip y el CIDR te sacan la subnetting a escanear. [ejemplo](https://www.ipaddressguide.com/cidr)

 [Back](../introduccionHacking.md)