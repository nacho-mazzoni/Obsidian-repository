# Elementos del manejo de inventarios:
### Inventario:
Es un stock de items guardados con organizacion para conocer la demanda del consumidor externa o interna.
### Demanda:
El inventario existe para conocer la demanda. Generalmente la demanda de items de inventario es dependiente o independiente.
#### Demanda Dependiente:
Productos que se usaran como partes de un producto final o para producir otro producto.
#### Demanda Independiente:
Productos finales de los que no depende el consumidor para fabricar o producir otra cosa.
###### En este estudio nos **enfocaremos** en las **demandas independientes**
### Costos de Inventario:
#### Carrying Costs: Cc
El costo de mantener productos en inventario, costo de retención.
Este costo varia con el nivel de inventario en stock y algunaz veces con el tiempo que lo tengamos guardado.
#### Ordering Cost: Co
El costo de ordenamiento del pedido. Expresado como precio por pedido y es independiente del tamaño del pedido.
###### Ordering cost reacciona inversamente a Carrying cost, si el tamaño de pedido Q aumenta y menos pedidos se necesitan por lo que el costo de Orden disminuye. sin embargo el costo de mantener el inventario aumentara debido al aumento de cantidad pedida Q
### Shortage Cost: costo de escacez
Se da cuando la demanda del consumidor no se puede cumplir por falta de stock. Si esta escaecez se mantiene permanentemente incluye las perdidas por las ventas no realizadas.

# Modelo EOQ clasico:
supuestos:
- La demanda se conoce con certeza y es constante en el tiempo
- no se permiten faltantes
- El tiempo para recibir los pedidos es constante
- El pedido se recibe todo al mismo tiempo

Cantidad de Pedido: Q, se recibe y se consume de manera constante.
Punto de Reorden: R; Cuando el stock de inventario decrece hasta este punto se realiza un nuevo pedido. (En este modelo R=0).
La cantidad de pedido optima Q* es la cantidad pedida que minimiza el costo de mantenimiento y orden. 
Estos dos costos actuan de manera inversa, si Q aumenta la cantidad de pedidos disminuye y aumentan los costos de mantenimiento de inventario.
#### Costo anual de pedido: Co
se computa multiplicando el costo por pedido por el numero de veces que se pide en un año.
Si la demanda anual es D y el tamaño del pedido es Q:
$$Costo Anual de Pedido = Co*D/Q$$
#### Costo anual de mantenimiento de inventario: Cc
Se obtiene multiplicando el costo anual de mantenimiento por unidad con el nivel promedio de inventario anual Q/2.
$$CostoAnualdeMantenimiento = Cc*Q/2$$
###### El costo anual de inventario total es la suma del costo anual de pedido y de mantenimiento
$$TC = Co*D/Q + Cc*Q/2$$
#### Tamaño óptimo de pedido para el modelo:
$$Q* = sqrt(2*Co*D/Cc)$$
#### Objetivo del modelo:
$$MIN TC(Q) = Co*D/Q + Cc*Q/2$$
#### Costo total anual:
Siendo P, el precio por unidad de producto pedido, podemos calcular el costo total anual de la siguiente manera:
$$Tc(Q)=P*D + Co*D/Q + Cc*Q/2$$
# Modelo EOQ Cantidad de Producción
Los supuestos que cambian en comparacion con el anterior modelo es que contiene una demanda diaria, o gradual (medida en dias),  y que el pedido no se recibe instantaneamente, sino que ingresan unidades segun una tasa diaria.
La cantidad de pedido se recibe gradualmente en el tiempo. El inventario se va agotando a la misma vez que se va reponiendo. 
En el modelo EOQ clasico el nivel de inventario medio es Q/2 pero en esta variacion el nivel de inventario maximo y medio son:
#### Nivel de inventario:
##### Maximo: 
$$Q*(1-d/p)$$
##### Medio:
$$(Q/2)*(1-d/p)$$
#### Definimos los siguientes parametros:
**p:** tasa diaria con la que se recibe el pedido. Conocida como tasa de producción.
**d:** tasa diaria de demanda de inventario.
La tasa de demanda diaria no puede superar la de produccion si asumimos que no puede haber faltantes.
Si p=d, no hay tamaño de orden debido a que los items se producen al mismo tiempo que se consumen. 
Para este modelo se tiene que p ≥ d.
#### Punto de Reorden:
$$R = d*L$$
siendo L la demora, o tiempo de espera para que llegue el pedido completo.
#### El tiempo para recibir un pedido:
Es el tamaño del pedido dividido por la tasa de producción.
$$Q/p$$
La cantidad de stock consumido durante este tiempo se obtiene, multiplicando a esta fórmula la tasa de demanda.
$$(Q/p)*d$$
#### Costo total de mantenimiento:
$$((Cc*Q)/2)*(1-d/p)$$
#### Costo anual total de inventario:
$$Tc(Q)= Co*D/Q + ((Cc*Q)/2)*(1-d/p)$$
#### Cantidad óptima de pedido:
$$Q* = sqrt((2CoD)/(Cc*(1-d/p)))$$
# Modelo EOQ con Descuento por Cantidad
El modelo EOQ basico puede ser utilizado para resolver la cantidad optima de pedido para este tipo de modelo. Sin embargo la aplicacion esta alterada, La ecuacion agrega el precio del producto en la determinada cantidad.
$$Tc(Q) = CoD/Q + CcQ/2 + PD$$
Cuando hay un descuento debido a la cantidad, este esta asociado a una determinada cantidad de pedido Q, La cual puede ser diferente de la optima, y el cliente evaluara la posibilidad de sacrificar mayores costos de mantenimiento de inventario por el descuento de la cantidad. Como resultado, el precio de compra afecta la cantidad optima de pedido cuando hay descuentos disponibles.
# Stocks de Seguridad:
Cuando la demanda es incierta, un stock de seguridad es añadido para cumplir con esa demanda mientras se espera por la producción.
