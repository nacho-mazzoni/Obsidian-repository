# Capa de enlace Nº = 2
- Si la capa física es mala necesito tener una capa de enlace muy robusta y viceversa.
- Depende de lo que tengo en la capa física defino el protocolo que voy a utilizar en la capa de enlace
###### Dentro de la capa de red el campo de carga se denomina paquete
###### Dentro de la capa de enlace el campo de carga se denomina trama

## Funciones de la capa de enlace
### obligatorias
- identificar tramas
- detección de errores

#### Técnicas de Entramado
- generar una violación en el código de capa física (tratamos de no usarla)
- secuencia de bits indicadora de inicio y final, con bits de relleno. (Técnica que define un carácter especial)
###### si en los datos aparecen cinco bits 1 se intercala un 0. luego el receptor siempre que haya cinco bits 1 seguidos el cero siguiente lo saco. No le importa 
- Caracteres de inicio y final, con caracteres de relleno
- Contador de caracteres, si erramos en un bit se desplaza todo el dato. Si un bit se pierde se pierde todo el dato. cuando ese dato se pasa a la capa de red no lo entiende.

#### Controlar el Flujo
 - Necesario para no aglobar al receptor
 - se realiza normalmente a nivel de transporte, también a veces a nivel de enlace.
 - Utiliza mecanismos de retro-alimentacion (el receptor advierte al emisor).
## Servicios
- no orientado a la conexión sin confirmación de recepción
- no orientado a la conexión con confirmación de recepción
- orientado a la conexión con confirmación de recepción
#### Orientado a la conexión: 
###### para comenzar una conexión debo solicitar permiso. http, orientado a conexión. Ethernet, no orientado a conexión. (No orientado a conexión en esta capa tarda, es malo).
#### confiabilidad: 
###### si yo te envió un dato, debo recibir confirmación de que llego. 

###### HDSL no orientado a la conexión y confiable.
