
# Fuzzing y enumeración de archivos en un servidor web

En esta clase, hacemos uso de las herramientas Wfuzz y Gobuster para aplicar Fuzzing. Esta técnica se utiliza para descubrir rutas y recursos ocultos en un servidor web mediante ataques de fuerza bruta. El objetivo es encontrar recursos ocultos que podrían ser utilizados por atacantes malintencionados para obtener acceso no autorizado al servidor.

Wfuzz es una herramienta de descubrimiento de contenido y una herramienta de inyección de datos. Básicamente, se utiliza para automatizar los procesos de prueba de vulnerabilidades en aplicaciones web.

Permite realizar ataques de fuerza bruta en parámetros y directorios de una aplicación web para identificar recursos existentes. Una de las ventajas de Wfuzz es que es altamente personalizable y se puede ajustar a diferentes necesidades de pruebas. Algunas de las desventajas de Wfuzz incluyen la necesidad de comprender la sintaxis de sus comandos y que puede ser más lenta en comparación con otras herramientas de descubrimiento de contenido.

Por otro lado, Gobuster es una herramienta de descubrimiento de contenido que también se utiliza para buscar archivos y directorios ocultos en una aplicación web. Al igual que Wfuzz, Gobuster se basa en ataques de fuerza bruta para encontrar archivos y directorios ocultos. Una de las principales ventajas de Gobuster es su velocidad, ya que es conocida por ser una de las herramientas de descubrimiento de contenido más rápidas. También es fácil de usar y su sintaxis es simple. Sin embargo, una desventaja de Gobuster es que puede no ser tan personalizable como Wfuzz.

En resumen, tanto Wfuzz como Gobuster son herramientas útiles para pruebas de vulnerabilidades en aplicaciones web, pero tienen diferencias en su enfoque y características. La elección de una u otra dependerá de tus necesidades y preferencias personales.

A continuación, te proporcionamos el enlace a estas herramientas:

- Wfuzz: https://github.com/xmendez/wfuzz
- Gobuster: https://github.com/OJ/gobuster
- otra erramienta es fuff que la utiliza cuando la web va muy lenta ya que es muy rapida la herramienta.

- Algo a tener en cuenta es que en el video se explica con la direccion `*.miwifi.com` entonces lo que dice savitar es que podemos hacer con el parametro `vhost` un reconocimiento para ver los distintos subdominios para "mifiwi.com" `por ejemplo: hola.miwifi.com` (tener en cuenta que habria que utilizar el diccionario de subdominios).

- Se pueden utilizar diferentes parámetros de Wfuzz para ajustar el alcance y la profundidad de nuestro reconocimiento en aplicaciones web. Algunos de los parámetros que cubriremos incluyen el parámetro ‘–sl‘, para filtrar por un número de líneas determinado, el parámetro ‘–hl‘ para ocultar un número de líneas determinado y por último el parámetro ‘-z‘ para indicar el tipo de dato que queremos usar de cara al reconocimiento que nos interese aplicar, abarcando opciones como diccionarios, listas y rangos numéricos.

- Como hacer para fuzzear por mas de 1 parametro?
 ```
  wfuzz -c  --hc=403,404 -t 200 -w <diccionario> -z list,<lista de parametros ej:html,pxp,txt> https://miwifi.com/FUZZ.FUZ2Z (SE PONE UN 2 ENTRE LAS Z).
 ```

- Como fuzzear por un rango?
 ```
  wfuzz -c  --hw=6515 -t 200 -z range,1-20000 'https://www.mi.com/shop/buy/detail?producto_id=FUZZ'.
 ```

[Back](https://lucasringuelet.github.io/introduccionHacking/reconocimiento.html)