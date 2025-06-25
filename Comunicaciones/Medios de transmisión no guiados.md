#### Medio tangible o Guiados: 
la energía va a ir guiada dentro de ese conductor de energía eléctrica, cable de cobre, de aluminio o una fibra óptica que va a guiar la luz dentro de la fibra 
#### Medio intangible o no Guiados:
No tangible porque no lo puedo ver ni tocar, no hay una guía para transmitir las ondas electromagnéticas en el aire. Mas allá de que luego con antenas podemos direccionarlas. Lo que pasa es que se irradian todas las ondas electromagnéticas en el ether (aire).
a nosotros nos interesa irradiar energías hacia donde esta la población.
# Transmisión Inalambrica:
### 2GHz to 40GHz
- microondas
- altamente direccional
- enlaces punto a punto
- satélites
### 30 MHz to 1GHz
- ominidireccional
- Broadcasting de radio
### 3 x10¹¹ to 2x10¹⁴
- infrarrojos
- Formato Local

## Antenas:
Conductor utilizado para irradiar o captar energía electromagnética. Recibe energía electrica y la convierte en señales electromagnéticas.
###### Transmisión de señal:
- energía eléctrica se convierte a energía electromagnética
- la conversión se realiza en la antena
- La energía se irradia al entorno que envuelve la antena
###### Recepción de la señal:
- La energía electromagnética se convierte a energía eléctrica
- La conversión se realiza en la antena.
- La energía eléctrica se pasa al receptor.
###### La misma antena es a menudo usada en ambos sentido.
## Patrón de Radiación:
- La potencia radiada es en todas las direcciones
- No es la misma performance en todas las direcciones
- Las antenas isotropicas teóricamente son un punto en el espacio.
	- irradian energía en todas las direcciones igualmente.
	- El diagrama de radiación es una esfera.
### Antena Parabólica de Reflexión:
- usadas para microondas terrestres y satélites
- Parábola es el lugar geométrico de todos los puntos que equidistan de una recta dada y de un punto fijo que no pertenecen a la recta
	- Punto: foco
	- recta: generatriz
- Cualquier fuente de EE* situada en su foco, seguirán trayectorias paralelas al eje de la parábola
	- Este efecto consigue un haz paralelo sin dispersión alguna.
- En el receptor, si las ondas recibidas son paralelas al eje de la parábola reflectante, la señal resultante estará concentrada en el foco
### Ganancia de una antena:
- es una medida de su direccionalidad
- se mide en dB
- dada una dirección, se define la ganancia de una antena como la potencia de salida en esa dirección comparada con la potencia transmitida en cualquier otra dirección por una antena omnidireccional.
- El área efectiva de una antena está relacionada con su tamaño físico y con su geometría y ella con la ganancia. 
$$G = 4π Aϵ / λ² = 4π f² Aϵ / c²$$
# Microondas terrestres:
La antena as común es la de plato.
#### Aplicaciones:
- Servicios de telecomunicaciones en reemplazo de cable coaxil o fibra
- Enlaces punto a punto entre edificios de corta distancia
#### Características de transmisión:
- rango de operación: 1 a 40 GHz
- Mayor frecuencia implica mayor ancho de banda.
- La principal causa de perdida es la atenuación
- La perdida la expresamos con:
$$L = 10log(4πd/λ²)[dB]$$
- La atenuación varia con el cuadrado de la distancia.
# Microondas por satelite:
- es una estacion que retransmite microondas
- el satelite recibe una frecuencia, amplifica o repite la señal y transmite en otra frecuencia
- Requiere orbitas geoestacionarias
- Televisiom, teléfono a grandes distancias, redes privadas de computadoras.
### Características de transmisión:
- Rango de operacion óptimo de 1 a 10 GHz.
Arriba de 10GHz existe mucha atenuación
- Rango muy usado: 5,925 y 6,424 GHz canal ascendente y 3.7 y 4.2 GHz canal descendente. Banda 4/6 GHz.
## Propagación Inalambrica:
#### La señal puede viajar por tres caminos:
- Ondas superficial: sigue el contorno de la superficie terrestre. Radio AM o FM
- Ondas aéreas
	- Radios amateur
	- la señal se refleja en la ionosfera.
- Linea de Vista LOS:
	- Arriba de los 30 MHz
	- el radio de horizonte afecta la transmisión
#### Transmisión por linea de vista:
- si no hay obstaculos, la linea de vista óptica se puede expresar cómo:
	- d=3,57 raiz(h).
	- d es la distancia entre la antena y el radio horizonte en kilometros y h es la altura en metros.
- La linea efectiva se expresa:
	- d=3,57 raiz(kh)
	- donde k es un factor de ajuste que tiene en cuenta la difracción
- El enlace completo se expresa:
	- 3,57 raiz(kh1) + 3,57 raiz(kh2)
	- h1 y h2 son las alturas de las torres
- Cualquier comunicacion inalambrica produce una dispersion de la señal con la distancia.
- a este fenomeno se lo llama: Perdida en espacio libre. $$- L(dB) = 20 log(f) + 20 log(d) - 147,5 dB$$
#### Zona de Fresnel:
- elipsoide de revolución
- eje mayor = eje del haz
- eje menor en la mitad del vano
- Criterio de obstrucción < 15% del área.
