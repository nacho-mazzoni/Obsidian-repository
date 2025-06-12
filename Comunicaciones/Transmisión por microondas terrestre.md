# Análisis de la transmisión con microondas
## Caracteristicas de la propagación
### Fundamentos de la propagación
##### Los enlaces de radio, o radioenlaces se realizan con "radiofrecuencia", es decir con señales que se encuentran en el espectro RF de microondas.
##### Trabajamos con ese nombre a señales de radio que se encuentran desde los 0,9 GHz en adelante, mas o menos, hasta los 30 MHz. La banda 10 (de 10^9 - 10^10) llamada de SHF o Super High Frecuency.
##### Una transmisión con RF requiere que la señal transmitida alcance a la antena receptora con la potencia necesaria para excitarla para que la señal recibida pueda ser copiada y decodificada sin errores irrecuperables. Cuando se verifica esta condicion, se dice que la antena receptora se encuentra alcanzada por el transmisor o tambien que esta en el area de cobertura de la antena emisora.
##### En la banda señalada, son importantes los fenomenos de reflexión, refracción, difracción e interferencia. La tecnica de modulación de la señal es importante porque con algunas de ellas se requiere que haya entre antenas una trayectoria recta y limpia, es decir, sin obstaculos ni elementos que produzcan dispersión. 
##### La linea recta entre puntas de antenas emisoras y receptoras será la trayectoria primaria para la propagación de la señal en estas frecuencias y se las suele llamar trayectoria de espacio libre para el haz [Tomassi]. El espacio entre ambas puntas de antena se llama *VANO*
##### Cuando esta trayectoria esta limpia y sin obstrucciones es cuando formalmente constituye una *Linea de Vista* o "LOS". (Line Of Sight).
##### La propagación de la señal no sufrira obstrucción del horizonte si las antenas estan a la altura correcta. Si ellas estan debajo de la altura correcta, el haz colisionara contra el terreno en el horizonte, sin alcanzar el objetivo. En tal caso diremos que no existe alcance visual.
##### Tecnologias emergentes como *HSPA/QAM*. Responden con valores elevados de *BER* cuando la señal no tiene linea de vista. Es conveniente que haya tal linea de vista para mantener un BER bajo y la velocidad binaria alta, aunque puede trabajar sin LOS. Algunas técnicas, son mas inmunes al desvanecimiento manteniendo el BER bajo cuando se generan dispersiones por obstáculos, auto referencia y otros fenómenos.

### El rol de la modulación
##### La modulación QAM : tasa de simbolos baja pero mejora las regiones de decisión de cada simbolo para igual tasa de simbolos, mejora el BER. La afectan frecuencias cercanas, auto interferencias y dispersiones modales, éstas, potencialmente la interfieran y la transmision resulta eventualmente con *fading* creciente con la distancia. Esto genera la necesidad de LOS.
##### OFDM: consiste en la utilizacion de una portadora formada por una importante cantidad de subportadoras que se encuentran en frecuencias proximas dispuestas ortogonalmente y por ello la transmmisión se comporta como una multitud de portadoras que se hubieran modulado cada una en una banda angosta en lugar de ser solo una en banda ancha. Asegura que haya baja interferencia intersímbolos [Tomasi] aplicando a la modulación de cada subportadora una técnica convencional como QAM, a baja velocidad de generación de simbolos.
##### La señal en su conjunto resulta robusta y una ventaja comparada con los métodos de portadora única o dual en cuadratura es la estabilidad en canales de comunicación con condiciones adversas, inestables o que presentan malas condiciones, generando un BER alto o creciente con la longitud del enlace.

## Cobertura de la instalación
##### A la distancia que recorre el haz desde la punta de su antena de propagación hasta aterrizar contra el horizonte, se llama *horizonte de radio*.

 ![[Calculo Horizonte del Radio.jpg]]
 
 
### El horizonte de radio
$$
 d(Km) = 3,58 * sqrt(H(m))
$$
##### El valor así obtenido del horizonte del radio se aplica ahora al calculo del vano máximo (Que llaaremos D) que puede lograrse en las peores condiciones cuando las alturas que se encuentran en las antenas son conocidas:
- Si la instalación es simétrica, ambas antenas se encuentran a la misma altura: $$ D(km) = 2d = 7,16*sqrt(H(m))$$
	- O en caso de que las alturas no sean las mismas: $$ D(Km) = 3,58*sqrt(H1(m)) + 3,58*sqrt(H2(m))$$
##### A estas formulas las llamamos *Cálculo abreviado del Horizonte del Radio* y permite encontrar el horizonte del radio en Km para la altura a la que se encuentra la antena expresada en metros, con un ligero error despreciable con respecto a la verdadera distancia, que es la distancia en arco.

### El efecto de la atmósfera
##### El alcance visual puede verse modificado por varios factores. La interacción de la onda con los campos gravitacionales tienen un papel importante pero aún más es la influencia de la refracción atmosférica [Tomasi] en las inmediaciones del horizonte.
##### El efecto que se observa, en general, es equivalente al hundimiento del horizonte como consecuencia de que la trayectoria de espacio libre no ocurre exactamente en el espacio libre, sino en un medio real como la atmósfera con índice de refacción distinto de 1.
##### Esto tiene un efecto sobre la velocidad de propagación del haz y ademas genera "tubos" de propagación en la atmosfera, que funcionan como conductores directivos, y que inducen al haz a curverse acompañando a la superficie de la tierra. Se pueden considerar estas interacciones sobre el haz como el efecto de un factor τ, tal que:
$$d(Km) = τ*3,58*sqrt(H(m)) $$
##### Esto forma un factor k denominado *factor de distancia* en el cálculo del horizonte de radio usado en el cálculo rápido y práctico del alcance visual, con el fin de determinar la viabilidad del enlace.
### Otros factores que intervienen en el cálculo
##### La cota de su basamento y considerar la diferencia de cota de la otra instalación con recpecto a la misma referencia.
--- 
##### Supones que el máximo radio de cobertura corresponde al máximo alcance visual teórico no es correcto y se debe acudir al sobredimensionamiento de la altura de la estructura de soporte cuando se deba asegurar el radio de cobertura, ya sea tomando margen o factor de seguridad, segun indique la circunstancia. 
### El despeje de la línea de vista
##### Una instalación con una antena de cualquier tecnologia y con cualquier tipo de modulación, siempre que este radiando de modo omnidireccional, genera un cono sobre el terreno. Aunque lógicamente en sentido figurado.
##### En realidad, toda la imagen es figurada ya que el verdadero aspecto es el de un haz que tiende a ser tangente a la tierra en el horizonte
![[Area de cobertura del cono.jpg]]
![[Análisis de altura.jpg]]
##### Para las instalaciones con modulaciones que requieren linea de vista despejada, es necesario que se calcule para el haz la *Altura de despeje* o Ad, que es la menor distancia desde el haz a la superficie de la tierra. 
##### Si existe un objeto que potencialmente producirá interferencia y está situado en el peor lugar, es decir en el lugar donde el haz más se acerca al perfil de la tierra, entonces la altura del haz es crítica.
##### Si la instalacion es simetrica, el punto de mayor acercamiento estara en la mitad del recorrido. $$d = D/2$$
##### y en ese mismo lugar se encontrara la menor distancia del haz a la superficie, es decir la altura crítica.
##### $$Ad = sqrt((r + H**2)-d**2) - r$$
##### Si en cambio la instalacion en asimetrica. Los tres son el radio de la tierra mas la torre mas baja, el radio de la tierra mas alta y el vano.
##### El analisis permite encontrar la altura A del haz a una distancia arbitraria L del origen.
##### puede obtener la distancia d desde la torre mas baja hasta el punto donde esta la altura de despeje crítica:
##### $$d = D**2 + H1**2 - H2**2 + 2r(H1-H2) / 2D$$
##### con d (distancia crítica) la altura crítica de despeje de Ad queda expresada por:
##### $$ A = sqrt((Ad + r)**2 + d`**2) - r$$
### Zona de Fresnel
##### A la recta que determina la linea de vista, y que se usa para calcular el despeje, se la suele llamar eje del haz. Rodeando a dicho eje, se encuentra una zona denominada Zona de Fresnel.
##### Esta zona actua como una region critica que no deberia ser invadida por ningun objeto, bajo riesgo de que se genere una difraccion que degrade adicionalmente la transmision. Mayor la invasion de la zona, mayor la magnitud de la degradacion de la señal.
##### Dicha zona tiene forma de elipsoide de revolucion. El elipsoide genera una zona espacial cuyo corte transversal al eje del haz muestra un área circular.

![[Zona de Fresnel.jpg]]
##### Se puede demostrar que no existe una unica Zona de Fresnel, sino infinitas. Cada una de ellas envuelve a la anterior. 
##### Se puede calcular el radio de una zona enesima en un punto genérico mediante la ecuación general
##### $$rn=548*sqrt(n*d1*d2/F*D)$$
##### Notese que d1, d2 y D están medidos en Km y la frecuencia F en MHz. Si bien corresponde formalmente a frecuencias de hasta 10 Mhz el error introducido es despreciable tomandolo para valores de frecuencia dentro del subespectro completo de microondas.
##### Ante esta circunstancia, podemos directamente calcular el radio que involucra la Zona de Fresnel como una única área (y no la sucesion de capas) directamente como:
$$r = 548*sqrt(d1*d2/F*D)$$
para todo d1, d2, D (Km), F(Mhz), r(m)
##### Este fenomeno no exige que exactamente nada invada esa zona crítica, sino que nos obliga a trabajar con un criterio de obstrucción.
##### Pero como criterio rector debería procurarse que el area obstruida no supere el 15% del area circular circular de la Z1 de Fresnel para no tener que calcular pérdidas adicionales por difracción.