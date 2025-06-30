# Cableado Ethernet
###### Dependiendo de los cableados definimos nodos. El nombre determina la velocidad de transmisión (bps). Todos basados en ethernet, y ademas se transmite en banda base.
![[CableadoEthernet.jpg]]
###### 10BASE5 y 10BASE2 son cables coaxiales que no se ven mas. En estos el router funciona como un host, una puerta de entrada y salida, puede estar en cualquier parte del tramo de cable, en un extremo, en el medio, etc. (Con 10BASE5 c/500m un repetidor)
###### 10BASEF: fibra óptica, máximos segmento 2000 m y cantidad de nodos/seg:1024.
![[TipoCableadoHUB.jpg]]
Este dispositivo HUB, solo se conecta a la PC y muestra si hay o no colisión (no toma otra acción).

![[codificacionEthernet.jpg]]
No se utiliza modulación, solo codificación.
Ethernet de 10Mbps funciona con manchester, de 100Mbps o 1Gbps no se pueden codificar con manchester, se usan tecnicas mejores con codificaciones sustitutivas. (Leer en Tannenbaum).
# Protocolo de la Subcapa MAC de Ethernet
![[ProtocoloSubCapaMACEthernet.jpg]]
###### Similar a HDLC pero no tiene un limite en la cantidad de datos. Porque no tengo header ni final line. 
###### Protocolo orientado al byte
###### Un host no se puede adueñar del canal por mas tiempo que del que le lleve leer los datos que reciba.
###### En HDLC no teníamos dirección origen. En este caso tenemos de origen y de destino. El host solo lee los que en dirección destino esta su dirección pero puede ver todos los mensajes que pasan por el cable.
###### Se puede hacer un broadcast para que todos los host reciban el mensaje que uno manda. 
###### Problemas en redes LAN: CONGESTIÓN.
###### Preámbulo: 8 bytes que son 0's o 1's. Sirve para sincronizar el receptor con el clock del emisor)  
###### Pad o Relleno: Si los datos son cero yo necesito que mi trama sea de 64 byte como mínimo. Inserta datos/basura para llegar a los 64 bytes de la trama (va de 0 a 46 bytes). Estos 64 bytes deben obtenerse sumando los tamaños de todos los datos menos el del preámbulo.

##### Tamaño minimo de trama: 64 bytes. ¿Porqué?
![[DibujoExplicaciónTamTrama.jpg]]
###### velocidad de la luz: c = 3x10⁸ m/s; NVP = 2x10⁸ m/s
###### $t_1 = 2500 m / 2x10⁸ m/s = 12,5 μs$
###### $t_2 = 2500 m / 2x10⁸ m/s = 12,5 μs$
###### $t_1 + t_2 = 25 μs$ --> $T_12 = 2*(t_1+t_2) = 50 μs$
###### Se multiplica por dos para considerar los repetidores y el retardo que tienen.
###### Tiempo de contienda = 2τ. 
con 10 Mbps en 50μs se transmiten 500 bits, equivalente a 62,5 bytes 
tomando como valor a 64 bytes, son 512 bits, transmitidos en 51,2 μs (Tiempo de contieda=2τ).
###### Si un host logra transmitir sin obstruccion por mas tiempo que el de contienda, el canal es suyo. 
###### Durante el tiempo de contienda <u>solo uno puede transmitir con exito</u>, si  otro transmite en ese intervalo hay una colision. 
###### Por lo subrayado es que no hay ack. 
![[DeteccionDeColision.jpg]]
## Para conexiones mas grandes (100 Mbps o 1 Gbps)
#### Tramas JumboFrames: 1500 bytes.
#### Juntar Tramas (Ethernet no lo permite).
