#### Series de Tiempo: 
Conjunto de datos observados de una variable medida en el tiempo a intervalos regulares, ordenado cronológicamente. Xt o X(t) con t discreto (año, meses, semanas).
#### Suposición:
Si una serie tiene un comportamiento particular en el tiempo hay una posibilidad de que ese comportamiento continúe en el futuro.
# Pronostico:
Predicción sobre el valor de una variable de una serie de tiempo de algún momento en el futuro.
### Características de los pronósticos:
- Casi siempre estarán equivocados
- da una medida de error
- Pronosticar unidades en conjunto es mas fácil que pronosticar unidades individuales
- Entre mas a futuro se realizan los pronósticos menos exactos serán.
# Pronósticos Objetivos
(Métodos con series de tiempo y regresión).

se realizan pronósticos con bases en datos históricos. Los pronósticos con series de tiempo utilizan solo la historia de la serie que se va a pronosticar, mientras que los modelos de regresión muchas veces incorporan el historial de otras series.
El objetivo es encontrar patrones predecibles y repetibles en los datos pasados.
Entre los patrones repetibles estarán la tendencia lineal creciente o decreciente, la tendencia curvilínea (incluyendo crecimiento exponencial) y las fluctuantes estacionales. Cuando usamos la regresión construimos un modelo causal que predice un fenómeno (la variable dependiente) con base a la evolución de uno o mas fenómenos distintos (las variables independientes). 
### Clasificación de los pronósticos cuantitativos:
1. Métodos de Pronósticos y suavizamiento Simple
2. Métodos de Regresión Lineal
3. Métodos de Análisis de Correlaciones y Modelo ARIMA (Promedio móvil integrado autoregresivo).
### Componentes de una serie de tiempo:
#### Tendencia:
Comportamiento de crecimiento o decrecimiento a largo plazo, de manera lineal o no lineal.
#### Series estacionales:
aquellas que tienen un patrón que se repite regularmente durante el mismo periodo de tiempo.
##### Variaciones estacionales:
se deben basicamente a causas climatologicas, vacacionales o fiscales.
#### Componente cíclica:
similar a la estacionalidad, excepto porque la duración y la magnitud del ciclo pueden variar. 
#### Componente aleatoria o ruido:
Representa la variabilidad que se puede dar en la variable analizada en la serie de tiempo.
###### los modelos de series de tiempo se estudian bajo el supuesto de que es estacionaria.
## Metodos para pronosticar series de tiempo estacionarias:
Una serie de tiempo exponencial es aquella en la que cada observacion puede representarse por medio de una constante mas una fluctuacion aleatoria. En simbolos:
$$Dt = µ + εt$$
donde µ es una constante desconocida que corresponde a la media de la serie y εt es un error aleatorio con media 0 y varianza τ².
### Metodos de Suavizacion: 
Suavizar fluctuaciones aleatorias causadas por...
### Promedios moviles: 
el termino movil indica que se movera el promedio a medida que surjan nuevas observaciones. 
El pronostico para el proximo periodo es el promedio de los K valores de datos mas recientes en la serie de tiempo es:
$$Ft+1 = (Yt + Yt-1 + ... + Yt-k+1)/k $$
- Para suavizar fluctuaciones a corto plazo.
La media de las observaciones K mas recientes se utiliza como pronostico para el proximo periodo. Notacion: PM(K) para los promedios moviles del periodo K.
### Alisado exponencial:
El pronostico para el periodo t+1 es un promedio ponderado del valor real en el periodo t y el valor actual de demanda.
nuevo pronostico = α (observacion actual de demanda) + (1-α)(Ultimo pronostico).
$$Ft+1 = α*Yt + (1-α)*Ft$$
donde 0<=α<=1 es la constante de suavizamiento.
Los valores pequeños de k o los valores grandes de α resultan de pronósticos que asignan mayor peso a los datos actuales.
Valores grandes de k y pequeños de α resultan de asignar pesos mayores a los datos pasados.
# Métodos Basados en la Tendencia:
Consideramos dos metodos de pronosticos que representan especificamente una tendencia en los datos: el analisis de regresion y el metodo de Holt.
### Analisis de regresion:
ajusta una linea recta a un conjunto de datos .
Sean (xi, Yi) datos apareados para las variales X e Y. Supongamos que Yi es el valor observado Y cuando Xi es el valor observado X. Creemos que existe una relacion entre X e Y que puede representarse mediante una linea recta:
$$Y=a+bX$$
La meta es encontrar los valores de a y b que mejor ajusten los datos. Los valores se eligen de manera que se minimice la suma de las distancias cuadráticas entre la linea de regresión y los puntos de datos.
![[problemaDeOptimizacion.jpg]]
![[problemaDeOptimizacion2.jpg]]
![[problemaDeOptimizacion3.jpg]]
### Suavizamiento exponencial doble, método de Holt:
El metodo de Holt es un tipo de suavizamiento exponencial doble que permite un suavizamiento simultaneo en la serie y la tendencia.
El metodo requiere de la especificacion de dos constantes de suavizamiento, α y β, y utiliza dos ecuaciones de suavizamiento: una para el valor de la serie (intercepcion) y una para la tendencia (pendiente). Las ecuaciones son:
$$Ft = α(At-1) + (1-α)(Ft-1 + Tt-1)$$
$$Tt = β(Ft - F(t-1)) + (1-β)T(t-1)$$
Ft intercepcion en el tiempo t y Tt el valor de la pendiente en el tiempo t. 
##### La segunda ecuacion puede explicarse así:
nuestro nuevo estimado de intercepcion provoca que modifiquemos nuestro estimado de pendiente en la cantidad Ft - Ft-1. este valor se promedia entonces con el estimado anterior de la pendiente Tt-1. 
Las constantes de suavizamiento pueden ser las mismas pero para la mayoría de aplicaciones se da mayor estabilidad al estimado de la pendiente β <= α.
El pronostico de τ pasos adelante, hecho en el periodo t se calcula como Fτ, t+τ de esta manera:
$$FITτ, t+τ = Ft + τTt$$
# Métodos para Series Estacionales
### Factores estacionales para series estacionarias:
Método sencillo para calcular los factores estacionales para una serie de tiempo con variación estacional y sin tendencia. 
1. Calcule la media de la muestra de todos los datos
2. Divida cada observación por la media de la muestra. Esto da los factores estacionales para cada periodo de datos observados.
3. Promedie los factores para los periodos semejantes dentro de cada estación. Esto es, promedie todos los factores correspondientes al primer periodo de una estación, todos los factores correspondientes al segundo periodo de una estación y así sucesivamente. Los promedios resultantes son los N factores estacionales. Siempre sumaran exactamente N.
# Exactitud de un Pronostico:
$et = Yt - Ft$
no es un buen calculo de error
$|et| = |Yt - Ft|$
Medidas mas usadas:
- Desviación absoluta media 
- Error cuadrático Medio.
![[Medidciondeerror.jpg]]
# Proceso de Pronostico:
1. Identificar el objetivo del pronostico
2. Recolectar datos históricos
3. Graficar datos e identificar patrones
4. Seleccionar un método de pronostico
5. Calcular el pronostico para los periodos históricos
6. Pronosticar el próximo periodo
7. Evaluar la exactitud del pronostico con una o mas medidas de errores
De 7 pasa al 4 si es que el metodo no ajusta bien.