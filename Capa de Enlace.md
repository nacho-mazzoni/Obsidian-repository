# Capa de enlace Nº = 2
- Si la capa fisica es mala necesito tener una capa de enlace muy robusta y viceversa.
- Depende de lo que tengo en la capa fisica defino el protocolo que voy a utilizar en la capa de enlace
Dentro de la capa de red el campo de carga se denomina paquete
Dentro de la capa de enlace el campo de carga se denomina trama

## Funciones de la capa de enlace
### obligatorias
- identificar tramas
- deteccin de errores

#### Tecnicas de Entramado
- generar una violacion en el codigo de capa fisica (tratamos de no usarla)
- secuencia de bits indicadora de inicio y final, con bits de relleno. (Tecnica que define un caracter especial)
si en los datos aparecen cinco bits 1 se intercala un 0. luego el receptor siempre que haya cinco bits 1 seguidos el cero siguiente lo saco. No le importa 
- Caracteres de inicio y final, con caracteres de relleno
- Contador de caracteres, si erramos en un bit se desplaza todo el dato. Si un bit se pierde se pierde todo el dato. cuando ese dato se pasa a la capa de red no lo entiende.

#### Controlar el Flujo
 - Necesario para no aglobar al receptor
 - se realiza normalmnete a nivel de transporte, tambien a veces a nivel de enlace.
 - Utiliza mecanismos de retroalimentacion (el receptor advierte al emisor).
## Servicios
- no orientado a la conexion sin confirmacion de recepcion
- no orientado a la conexion con confirmacion de recepcion
- orientado a la conexion con confirmacion de recepcion
#### Orientado a la conexion: 
para comenzar una conexion debo solicitar permiso. http, orientado a conexion. Ethernet, no orientado a conexion. (No orientado a conexion en esta capa tarda, es malo).
#### confiabilidad: 
si yo te envio un dato, debo recibir confirmacion de que llego. 

###### HDSL no orientado a la conexion y confiable.
