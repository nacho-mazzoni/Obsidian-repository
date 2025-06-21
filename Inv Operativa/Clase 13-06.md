## Alisado exponencial ajustado
beta: parametro para controlar cuanto cambia la tendencia con el cambio reciente, valor entre 0 y 1.
1. Defino el alpha
2. Para beta, ver cual ajusta mejor el valor de At (Prononstico con ajuste)

## Metodos Causales
### Regresion lineal:
y = a+b.x
Series de tiempos no estables con tendencia lineal a largo plazo
#### Ajuste lineal de tendencia:
regresión lineal q relaciona la variable dependiente con el tiempo.

Problema de optimización
![[problemaDeOptimizacion.jpg]]
![[problemaDeOptimizacion2.jpg]]
![[problemaDeOptimizacion3.jpg]]
Condición suficiente, d es una función convexa, luego es mínimo global del problema

## Ajuste factor estacional
un patrón estacional es un aumento o disminución repetitivo de la demanda 
### Método de ajuste Estacional:
aplica un factor estacional a un pronostico para obtener un pronostico estacionado.
el método mas sencillo es el método multiplicativo.
 Di : datos de la serie en diferentes años
 (buscar formula S_i)

Exactitud del pronostico:
$et = Yt - Ft$
no es un buen calculo de error
$|et| = |Yt - Ft|$
Medidas mas usadas:
- Desviación absoluta media 
- Error cuadrático Medio.

Proceso de Pronostico:
1. Identificar el objetivo del pronostico
2. Recolectar datos históricos
3. Graficar datos e identificar patrones
4. Seleccionar un método de pronostico
5. Calcular el pronostico para los periodos históricos
6. Pronosticar el próximo periodo
7. Evaluar la exactitud del pronostico con una o mas medidas de errores
De 7 pasa al 4 si es que el metodo no ajusta bien.

alpha y beta: elegimos el valor que mejor aproxima el pronostico
