## Alisado exponencial ajustado
beta: parametro para controlar cuanto cambia la tendencia con el cambio reciente, valor entre 0 y 1.
1. Defino el alpha
2. Para beta, ver cual ajusta mejor el valor de At (Prononstico con ajuste)

## Metodos Causales
### Regresion lineal:
y = a+b.x
Series de tiempos no estables con tendencia lineal a largo plazo
#### Ajuste lineal de tendencia:
regresion lineal q relaciona la variable dependiente con el tiempo.

Problema de optimizacion
**(Agregar fotos)**
Condicion suficiente, d es una función convexa, luego es minimo global del problema

## Ajuste factor estacional
un patron estacional es un aumento o disminucion repetitivo de la demanda 
### Metodo de ajuste Estacional:
aplica un factor estacional a un pronostico para obtener un pronostico estacionado.
el metodo mas sencillo es el metodo multiplicativo.
 Di : datos de la serie en diferentes años
 (buscar formula S_i)

Exactitud del pronostico:
$et = Yt - Ft$
no es un buen calculo de error
$|et| = |Yt - Ft|$
Medidas mas usadas:
- Desviacion absoluta media 
- Error cuadratico Medio.

Proceso de Pronostico:
1. Identificar el objetivo del pronostico
2. Recolectar datos historicos
3. Graficar datos e identificar patrones
4. Seleccionar un metodo de pronostico
5. Calcular el pronostico para los periodos historicos
6. Pronosticar el proximo periodo
7. Evaluar la exactitud del pronostico con una o mas medidas de errores
De 7 pasa al 4 si es que el metodo no ajusta bien.

alpha y beta: elegimos el valor que mejor aproxima el pronostico
