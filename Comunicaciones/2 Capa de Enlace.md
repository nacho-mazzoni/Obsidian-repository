# Capa de enlace Nº = 2
- Si la capa física es mala necesito tener una capa de enlace muy robusta y viceversa.
- Depende de lo que tengo en la capa física defino el protocolo que voy a utilizar en la capa de enlace
###### Dentro de la capa de red el campo de carga se denomina paquete
###### Dentro de la capa de enlace el campo de carga se denomina trama

## Funciones de la capa de enlace
### obligatorias
- identificar tramas
- detección de errores
### Opcionales (Servicio orientado a conexión)
* control de flujo
* corrección de errores
#### Técnicas de Entramado
- generar una violación en el código de capa física (tratamos de no usarla)
- secuencia de bits indicadora de inicio y final, con bits de relleno. (Técnica que define un carácter especial)
###### si en los datos aparecen cinco bits 1 se intercala un 0. luego el receptor siempre que haya cinco bits 1 seguidos el cero siguiente lo saco. No le importa 
#### Técnicas de identificación de tramas
- Caracteres de inicio y final, con caracteres de relleno
- Contador de caracteres, si erramos en un bit se desplaza todo el dato. Si un bit se pierde se pierde todo el dato. cuando ese dato se pasa a la capa de red no lo entiende.
![[IdentificadorDeTramas.jpg]]
#### Controlar el Flujo
 - Necesario para no agobiar al receptor
 - se realiza normalmente a nivel de transporte, también a veces a nivel de enlace.
 - Utiliza mecanismos de retroalimentación (el receptor advierte al emisor).
	 - requiere un canal semi-duplex o full-duplex
	 - no se utiliza en emisiones multicast/broadctast
- suele ir unido a corrección de errores
- no debe limitar la eficiencia del canal
## Servicios
- no orientado a la conexión sin confirmación de recepción
- no orientado a la conexión con confirmación de recepción
- orientado a la conexión con confirmación de recepción
#### Orientado a la conexión: 
###### para comenzar una conexión debo solicitar permiso. http, orientado a conexión. Ethernet, no orientado a conexión. (No orientado a conexión en esta capa tarda, es malo).
#### confiabilidad: 
###### si yo te envió un dato, debo recibir confirmación de que llego. 

###### HDSL no orientado a la conexión y confiable.

### Tipo de Transmisión 
#### Asíncrona:
###### cada byte se envía de forma independiente. Cuando no hay datos que enviar la linea esta en silencio.
![[transmisionAsincrona.jpg]]
#### Síncrona: 
###### La trama se envía sin separación entre los bytes. Cuando no hay nada que enviar el emisor envía una secuencia determinada de forma ininterrumpida para asegurar que no se pierde el sincronismo.

### Tasa de errores (BER)
###### La tasa de errores de un medio de transmisión se mide por la BER (Bit Error Rate) que se define como: 
###### bits erróneos/bits transmitidos
### Códigos de control de errores: 
###### Los códigos pueden ser: 
- detectores de errores
- Correctores de errores
###### Los códigos detectores tienen menos overhead
![[ControlErrores.jpg]]
## Protocolos de Parada/Espera
###### Protocolo orientado a conexión mas sencillo
###### El emisor va a mandar un dato avisando que lo manda y espera el mensaje del receptor para que le diga que llego sin errores
###### Este enlace es bidireccional pero no a la vez.
###### *La eficiencia de este protocolo es mala porque el 80% del tiempo esta parado*
![[ProtocoloParadaEspera.jpg]]
## Protocolos con Ventana deslizante
###### Se mejora con un enlace full-duplex. Puede enviar mensajes de ida y vuelta en ambos sentidos: *Ventana Deslizante*
###### Cuando llega el ack de la trama recién puedo borrarla del buffer. Este almacena las tramas y esta del lado del emisor.
![[ProtocoloVentanaDeslizante 1.jpg]]
#### Tamaño de la ventana
###### La ventana mínima para 100% de ocupación es la que "llena el hilo" de datos en ambos sentidos +1 
$W = 2τ*v/t + 1$ 
- w: tamaño de la ventana
- τ: tiempo de propagación 
- v: velocidad de la linea
- t: tamaño de la trama
###### Cuando se envían todas las tramas por el tamaño de la ventana deslizante el emisor para porque a esta altura ya debería haber recibido el primer ack. 
###### Número de secuencia: número de tramas consecutivas que puede enviar.

#### El Protocolo puede ser: 
- Retroceso n: no se acepta una trama hasta haber recibido las anteriores.
- Repetición selectiva: Se admite cualquier trama en el rango esperado y se pide solo la que falta.
![[RepSelectivayRetrocesoN.jpg]]
###### Repetición selectiva es mas complejo pero mas eficiente, y requiere mas espacio en buffers en el receptor.
###### Si hay un buffer en el receptor puedo almacenar las tramas hasta que una llegue errónea y vuelva a llegar bien. También puede descartar las que llegan después de la que llego mal y esperar que el emisor mande todas las tramas que le siguen a la errónea.
###### Tamaño de la ventana: 
- Retroceso n: número de secuencia-1
- Repetición selectiva: Número de secuencia/2
## Protocolos de nivel de enlace: HDLC, PPP(Internet) y LAP-F(Frame Relay)
### Protocolos HDLC (High level data link control)
- HDLC es un estándar ISO. Deriva del SDLC desarrollado por IBM.
- Protocolo de ventana deslizante muy completo
![[FormatodeTramaHDLC.jpg]]
![[TiposdeTramaHDLC.jpg]]
![[ComandosHDLC 1.jpg]]
#### Elaboración de Tramas HDLC:
##### En el emisor
###### 1. Concatenar campos de dirección, control y datos
###### 2. Calcular el CRC de la cadena resultante
###### 3. Realizar el relleno de bits poniendo un bit a cero siempre que en la cadena a enviar aparezcan cinco unos seguidos
###### 4. Añadir a la trama los delimitadores de inicio y final (01111110). si se envían dos tramas seguidas el delimitador de final de una sirve como inicio de la siguiente
##### *El receptor procede de manera inversa*
*CRC control de redundancia cíclico (Control de Errores)*
*dirección siempre es 111111111 (Broadcast), salvo en lineas multipunto*
###### El campo control es el que se encarga de todas las tareas del protocolo. los datos son cualquier trama con longitud>=0 igualmente se definen con los delimitadores.
*Tiene problemas con los buffer por este motivo*

### Protocolo PPP (Point to Point Protocol)
- protocolo de enlace característico de Internet, que se utiliza en :
	- Lineas dedicadas punto a punto
	- conexiones RTC analógicas o digitales (RDSI)
	- Conexiones de alta velocidad sobre enlaces SONET/SDH
- Puede funcionar de forma síncrona o asíncrona (Puerto COM de una Pc)
- es multi-protocolo, una comunicación soporta simultáneamente varios protocolos a nivel de red.
#### Características
###### delinea sin ambigüedades el final de una trama y el inicio de la siguiente
###### Puede eliminar el campo dirección
###### Protocolo de enlace para activar lineas, probarlas, negociar opciones y desactivarlas
###### Protocolo de enlace para negociar opciones de capa de red con independencia del protocolo de red usado. El método consiste en tener un NCP (Protocolo de control de Red) distinto para cada protocolo de capa de red soportado
![[TramaPPP.jpg]]
#### Componentes de PPP 
- LCP Link Control Protocol
- NCP Network Control Protocol
- CHAP Challenge Handshake Authentication Protocol

##### Funcionamiento de CHAP 

#### Nivel de enlace en Frame Ready
- No se realiza reenvío en caso de error
- El campo de dirección contiene la informacion del circuito virtual y los parametros propios de las funciones de Frame Relay
## Nivel de Enlace en ATM
###### Corresponde a la subcapa TC (Transmission Convergence) de la capa fisica del modelo ATM
###### Estructura de una celda ATM

###### Estructura de la cabecera de celda ATM

### Identificación de celdas ATM
- *Las celdas no llevan un delimitador. Para averiguar donde empiezan se usan dos tecnicas:*
###### 1. Caracteristicas del medio fisico
###### 2. Tanteo del HEC: se busca el flujo de bits recibido una secuencia de 40 bits en la que los ocho ultimos sean el HEC de los 32 primeros. Cuando se encuentra uno valido se confirma en las cuatro celdas siguientes.