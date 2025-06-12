## Definición de software
###### Conjunto de programas, instrucciones y datos que permiten que un dispositivo funcione y realice tareas especificas.
###### Es lo que le da vida al hardware.
### Particularidades del Software
- ###### Intangible: no se puede tocar, pero es esencial para que el dispositivo funcione.
- ###### Flexible: se puede modificar, actualizar y adaptar para cumplir diferentes propósitos.
- ###### Dualidad con el hardware.
- ###### Evoluciona rápidamente.

## Ingeniería de Software
###### "La aplicación de un enfoque sistemático, disciplinado y cuantificable al desarrollo, operación y mantenimiento del software; es decir, la aplicación de la ingeniería de software"
No solo se trata de programar.
###### Enfoque sistematico: sigue un proceso bien definido de pasos estructurados.
###### Disciplinado: se aplicanprincipios y metodologias comprobadas.
###### Cuantificable: se pueden medir aspectos clave, como rendimiento, calidad y costos.
### Principios Claves:
- modularidad
- abstracción
- dividir y conquistar
- generalización y reutilización
- estandarizacion
- gestión de calidad
- optimizacion de recursos

### capas:
- herramientas
- métodos
- procesos
- calidad
## Proceso de Software
###### Un conjunto de actividades, acciones y tareas. No es algo rígido.
- ###### Actividad: logra un objetivo amplio
- ###### Acción: conjunto de tareas que producen un producto importante del trabajo. Contenida dentro de la actividad.
- ###### Tarea: se centra en un objetivo pequeño, desarrollada dentro de las actividades.

### Estructura de un Proceso:
- Comunicación
- Planeacion
- Modelado
- Construcción
- Despliegue
###### Iteraccion --> Incremento del software
###### Se complementan mediante actividades sombrilla.
### Actividades Sombrillas
- aseguramiento de la calidad
- revisiones técnicas
- medición
- administración de la configuración
- administración dela reutilizacion
- seguimiento y control del proyecto
- administración del riesgo
### Mitos de software
#### Mitos de la Administracion
- Libro lleno de estándares
- Agregar programadores si nos atrasamos
- Subcontratar y descansar
#### Mitos del cliente
- El cambio se asimila con facilidad ya que el software es flexible.
- Para arrancar, basta solo con el enunciado general del objetivo.
#### Mitos del Profesional:
- Hasta que no corra no podemos evaluar la calidad
- El único entregable es el programa que funciona
- La ing. de software hará que generemos documentación innecesaria.

## Modelos del Proceso
###### Estructura de proceso general para la ing. de software.
- Comunicación
- Planeacion
- Modelado
- Construccion
- Despliegue
###### Con actividades sombrillas transversales
![[flujosdelproceso1.png]]![[flujodelproceso2.png]]
###### Al finalizar libero el incremento de software y vuelvo a comenzar.

![[flujodelproceso3.png]]
###### En algún momento del tiempo puedo hacer mas de 1 etapa.
### Modelos de Procesos prescriptivos:
- Buscan generar estructura y orden
- Pueden incluir las actividades estructurales pero cada uno pone distinto énfasis en ellas.
#### Modelo de cascada: 
###### Flujo lineal
![[modelodecascada.png]]
####  Modelo en V:
###### En paralelo se realizan o desarrollan pruebas a medida que avanzamos. Cuando el producto esta listo avanzamos con las pruebas
![[modeloenV.png]]
#### Modelo de proceso incremental: 
###### Permiten ir integrando parte del producto. Se pueden realizar actividades en paralelo.
![[modeloincremental.png]]
#### Modelo de proceso evolutivo:
##### Prototipo:
###### Busca desarrollar algo rápido que de valor al cliente
![[modeloevolutivo.png]]
##### Espiral:
###### En cada iteracion debemos analizar las entregas anteriores y pasa por todas las fases. Ayuda a gestionar los riesgos y costos.
![[modeloevolutivoenespiral.png]]

## Modelos de Procesos Ágiles
###### Periodo mas corto de desarrollo y entrega --> mayor tasa de éxito en los proyectos
###### Los avances se miden en entregas que agreguen valor al cliente.
### Manifiesto Ágil
#### Valores:
- Individuos e interacciones sobre procesos y herramientas
	- Las personas son el principal factor de éxito del proyecto.
- Software funcionando sobre documentación extensiva
	- No producir documentos a menos que sean necesarios de inmediato para tomar una decisión importante.
	- Medir avance en función de resultados intermedios --> "Ilusión de Proceso"
- Colaboración con el cliente sobre negociación contractual
- Respuesta ante el cambio sobre seguir un plan
	- planificación flexible y abierta
#### Principios:
- mayor prioridad --> satisfacer al cliente mediante la entrega temprana y continua de software con valor.
- aceptamos que los requisitos cambien, incluso en etapas tardías del desarrollo. Aprovechamos el cambio para proporcionar ventaja competitiva al cliente.
- Entregamos software funcional frecuentemente.
- Los responsables de negocio y desarrolladores trabajamos juntos durante todo el proyecto.
- Los proyectos se desarrollan en torno a individuos motivados.
- Comunicación eficiente y efectiva: cara a cara.
- El software funcionando es la medida principal de progreso.
- Los procesos ágiles promueven el desarrollo sostenible.
- La atención continua a la excelencia técnica y al buen diseño mejora la agilidad. 
- La simplicidad, es esencial
- equipos auto-organizados
- Reflexionar sobre como ser mas efectivos para ajustar y perfeccionar su comportamiento de manera regular.
### Scrum
###### Donde se aplica? En modelos complejos y prácticas emergentes.
###### Marco de trabajo, hace frente a problemas complejos a medida que se realizan entregas de valor.
###### Que no es scrum: 
- no es un proceso completo
- no es una metodología
#### Principios:
- individuos e interacciones sobre procesos y herramientas.
- Software funcionando sobre documentación extensiva
- Colaboración con el cliente sobre la negociación contractual
- Respuesta al cambio sobre seguir un plan.
#### Valores:
- Foco
- Coraje
- Apertura
- Compromiso
- Respeto
#### Pilares: 
- Transparencia
- Inspección (proceso y producto)
- Adaptación
#### Roles: 
- equipo de desarrollo
	- Liberan un incremento al final de cada sprint.
	- Equipo auto-organizado
	- Entre 3 y 9 miembros
	- Responsable de las estimaciones
	- Responsable de construir un incremento al final de cada sprint
- scrum master: 
	- responsable de que el equipo comprenda y utilice Scrum
	- Liderazgo servil
- Product owner:
	- representa al negocio, stakeholders, clientes y usuarios finales.
	- maximiza el valor.
	- gestión del product backlog.
#### Artefactos:
- Product backlog: 
	- listado ordenado de las funcionalidades de nuestro producto
	- priorización por valor de negocio o ROI
	- es dinámico
	- cada ítem debe tener un tamaño
###### Los ítems no son tareas, son funcionalidades completas.
- Sprint backlog:
	- PBI's seleccionados en el sprint
	- se descompone en tareas
	- todo sprint debe tener un objetivo
###### Todas las funcionalidades que van a incluirse en el sprint que estamos
- Incremento: 
	- resultado del cada sprint
	- debe cumplir con la definición de terminado
###### Producto que entregamos al terminar cada sprint, funcional y de valor para el cliente.
###### Definición de terminado: El conjunto de desarrollo, junto con el project owner deben definir qué es algo terminado para ambos.
#### Eventos:
##### Sprint:
- periodo de tiempo fijo (no mas de 1 mes)
- se ajusta el alcance ante retrasos o adelantos.
- lo puede cancelar solo el product owner.
##### Sprint planning: 
###### donde se define el sprint backlog
- define que es lo que se debe entregar y como realizarlo.
##### Scrum daily o diario:
###### reunión diaria para sincronizar, explicar en que avanzo cada uno y las dificultades que tuvieron.
###### Preguntas:
- ¿Qué hice?
- ¿En qué estoy?
- ¿Qué me bloquea?
###### Los bloqueos no se resuelven en esta reunión.
##### Revision de sprint:
###### Al finalizar cada sprint, se evalúa el incremento funcional.
##### Retrospectiva:
###### Fomenta la mejora continua y las buenas practicas
###### Centrado en el proceso. ¿Como fue?, ¿Como se puede mejorar?.
#### Refinamiento del product backlog:
- Actividad constante a lo largo de todo el sprint
###### Objetivo: detectar riesgos, profundizar PBI's del backlog y estimarlos.
## Kanban
###### A través de tarjetas tener un tablero general para ver en donde y en qué está trabajando el equipo.
###### Se basa en tres principios:
- Visualizar
- Limitar le trabajo en proceso
- Gestionar el flujo de trabajo
#### Visualizar: 
- las tareas se representan como tarjetas que avanzan de izquierda a derecha a medida que progresan.
- cuando el trabajo se hace visible, espera lograr un alto impacto.
###### Poder ver de cada una de las tareas a realizar el estado en el que esta.
#### Limitación del  trabajo en progreso: WIP
###### Se basa en lograr la fluidez de las tareas lo mas rápido posible. 
###### Focalización, define un grupo de tareas que puede terminar rápido.
###### WIP: work in progres. Limitar en cada columna la cantidad de tareas que puedo hacer concurrentemente.
#### Gestión del flujo de trabajo:
###### Hacer que el flujo de trabajo fluya rápidamente sin interrupciones.
###### Se trata de una mejora continua.
### Hacer Explicitas las Reglas del Proceso:
- ###### Todos deben comprenderlas para poder mover tareas entre etapas.
### Mejora Continua [[Kaizen]]
- ###### Los equipos revisan periódicamente su flujo de trabajo para detectar oportunidades de mejora.