# Planta automatizada

## Propuesta de planta automatizada

<img width="676" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/720cabd6-a22f-4ab4-8a29-0c245d9ec3bf">

Para la propuesta de proyecto, se propone la automatización de los procesos que implican un mayor riesgo para los trabajadores, y al mismo tiempo son los mas críticos en cuanto a la repetibilidad, velocidad, y calidad del producto final, es decir los procesos de corte, específicamente el acabado de bordes, y el taladrado, de tal forma que el proceso de ensamblado, empaquetado y posteriores, seguirían teniendo la intervención humana.

En la siguiente imagen se muestra un esquema general de la propuesta, en el lado izquierdo se encuentra la entrada de laminas de MDf precortadas mediante las maquinas corte laser que ya cuenta la manufactura no automatizada. Las laminas ingresan a una maquina CNC que se encarga de terminar el corte y acabar los bordes, de tal forma que la fresa tiene un menor desgaste y se aprovecha la maquinaria de corte laser presente en el proceso manufacturero previo a la automatización.

![image](https://github.com/APM-Kullu/Project/assets/52173621/fc2a4967-f346-4023-a35b-604b166bed51)

Las laminas salen de la fresadora CNC por medio de una cinta transportadora, donde se evacuan los residuos del corte, y un robot antropomórfico recoge las piezas resultantes, y las ingresa a un celda de taladrado. De igual forma este mismo robot se encarga de recoger las piezas terminadas del taladrado y las ingresa en un contenedor de salida, que un operario puede retirar cada vez que se requieran mas piezas para el siguiente proceso.


En la siguiente imagen se presenta un esquema de vista superior de la celda de taladrado. esta consta de dos cintas transportadoras que forman un ciclo, de tal forma que el robot antropomórfico ingresa o retira las piezas en el modulo de la parte superior, y el taladrado se ejecuta en el modulo de la parte inferior. Las piezas transitan a lo largo de la cinta transportadora, a traves de un plantilla que asegura las piezas, de tal forma que cuando lleguen a cualquiera de los dos módulos, el posicionamiento de las piezas sea el mismo, y se pueda realizar el pick and place del robot o el taladrado de forma precisa.

![image](https://github.com/APM-Kullu/Project/assets/52173621/37b42a9d-8136-468d-8335-696c3f1047f2)

En el diagrama anterior, también se especifican dos mecanismos de sujeción de plantillas, y sensores de detección de pieza, la idea consiste en detectar la presencia de una platilla cada vez que pase por el sensor, y en ese momento activar un mecanismo de fijación de la plantilla, que tenga una capacidad de autocentrado, de tal forma que la pieza se sujete en el mismo lugar en cada iteración del proceso. En la siguiente imagen se muestra un diagrama representando la vista frontal de dicho mecanismo.

![image](https://github.com/APM-Kullu/Project/assets/52173621/5fce7348-68f8-4e12-ab3e-61cdf9779059)

En la siguiente imagen se muestra una vista superior de la celda del robot, la idea de este sistema radica en tener la capacidad de recoger las piezas a la salida de la fresadora CNC e ingresarlas a la celda de taladrado, o retirarlas una vez terminado el proceso, ademas de poder reorientar las piezas en caso de que requieran agujeros en diferentes planos, e ingresarlas en otra plantilla para taladrar en el otro plano, por este motivo se plantea la necesidad de utilizar un robot antropomórfico que permita lograr cualquier orientación de la pieza, acompañado de un gripper de tipo ventosa neumática que permita sujetar diferentes geometrías de pieza sin tener que cambiar la herramienta.

![image](https://github.com/APM-Kullu/Project/assets/52173621/c0c23994-a643-4189-a161-47cde7a646e2)


## CNC

La estación de corte CNC recibe una lámina de MDF y entrega la lámina con los cortes de los patrones requeridos (2), los cuales se entregan de forma intercalada.

<img width="374" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/6dfb3aee-a7e8-4f87-9640-14275d7d5b1a">

### Cortes resultantes
<img width="427" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/c8bb30a5-803f-4fe1-9199-1f7075a3c523">
<img width="401" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/8e750e16-7b96-472a-b4d2-335dba94c087">

## Celda robotizada

La estación de la celda robotizada recibe la lámina de MDF cortada y organiza cada pieza en 4 templates para su posterior taladrado.

[Sección completa de la estación del brazo robótico](https://apm-kullu.github.io/kulluWebSite/robotica/)


## Banda transportadora en ciclo

La estación de la banda transportadora en ciclo, entrega un template a la estación del brazo robótico y cuando esto lo llena con las piezas correspondiente, se acciona, moviendo el template lleno a la cola de la estación de taladrado y dejando un template vacio para la estación del brazo.

<img width="408" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/e5324434-63f2-40eb-9265-c4045b87f2c3">

## Taladrado

La estación de taladrado recibe los templates llenos de piezas de la cinta transportadora y devuelve el mismo template con las piezas taladradas

<img width="450" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/8a926470-1f7e-480d-bf90-04f5a03dad38">



# Simulaciones de Corte

En este [documento](./PiezasYCortes.md) se describen algunos detalles que se deben tener en cuenta en el proceso de corte, como la modificación de los planos de corte, asi como la velocidad de corte y la simulación de estos procesos.

# Diseño a detalle de planta automatizada

En la siguiente imagen se muestra el diseño CAD de toda la planta automatizada, el cual es utilizado para la simulación mediante el software NX Mechatronics  Concept Designer. Se aclara que el robot que se muestra en el ensamble es de carácter representativo.

![](../images/assembly.png)

La planta ocupa una area de aproximadamente 10.5m x 9.5m, ocupados principalmente por 3 cintas transportadoras, una fresadora CNC, y un robot antropomórfico.

Los componentes comerciales que se utilizaron para el diseño de la planta automatizada, omitiendo los individuales de cada mecanismo son los siguientes:

La maquina CNC seleccionada es la que se muestra en la siguiente imagen, disponible [aquí](https://cntmotion.com/solutions/application/feed-through-parts-machining/)

![](../images/CNCMachine.png)

- Se utilizan 3 cintas transportadoras como la que se muestra a continuación, disponible en este [enlace](https://www.grainger.com/product/BESTFLEX-Powered-Roller-Conveyor-24-5YDF4?opr=PDPRRDSP&analytics=dsrrItems_5YDF3), cada una de una longitud de 24 pies (aproximadamente 7.3m) y un ancho de 24 pulgadas (61cm).

![](../images/conveyorMachine.png)

- Para cada cinta transportadora, se utiliza un sensor para detectar la llegada de una pieza, la referencia seleccionada se encuentra disponible [aquí](https://www.mcmaster.com/7674K812/).

- PLC [1769-L30ER ALLEN-BRADLEY](https://co.wiautomation.com/allen-bradley/plc-sistemas/compactlogix/1769L30ER?gclid=Cj0KCQjw7PCjBhDwARIsANo7CgmpGsCVsYg1hpT3X5nnFjPaax9bad99TBPo--CAxjIbJZAdXeUibbYaAoEbEALw_wcB) con sus correspondientes modulos de entradas y salidas digitales, [1756-IV32 ALLEN-BRADLEY](https://co.wiautomation.com/allen-bradley/modulos/controllogix/1756IV32). y [1756-OV32E ALLEN-BRADLEY](https://co.wiautomation.com/allen-bradley/modulos/controllogix/1756OV32E).

![](../images/plc.png)



# Plantillas de sujeción de piezas

Las plantillas se proponen como un ensamble de platinas de aluminio de 50mm de espesor, con perforaciones de 8mm de diámetro, para permitir el paso de tornillos M8 de 100 mm de largo, de tal forma que el armazón completo se puede ensamblar usando 96 de estos tornillos. En las dos imágenes que se muestran a continuación se observan las dos partes principales del armazón, donde la parte roja sirve como sostén para toda la plantilla, y ademas cuenta con agujeros diseñados específicamente para el autocentrado de la plantilla con la mordaza neumática, y la parte verde es la que sostiene la geometría de la plantilla donde se alojan las piezas. Todas las platinas fueron diseñadas teniendo en cuenta que se puedan manufacturar en una fresadora vertical convencional de ejes y asi facilitar su producción y remplazo en el mercado local.

![](../images/template_p1.png)
![](../images/template_p2.png)

La pieza ensamblada tiene un tamaño total de 850mm x 24 pulgadas (609.6mm) acorde con el ancho de la cinta transportadora.

Por otro lado se diseñaron 4 geometrías en madera de MDF de 30mm, las cuales pueden ser ensambladas mediante el corte de laminas de 15mm, de tal forma que no se requieran capacidades de manufactura adicionales a las que ya cuenta la planta previo a la implementación de las celdas de manufactura automatizada.

A continuación se presentan las 4 geometrías propuestas, junto con las piezas de corte, con el fin de representar la distribución de las piezas durante el proceso de producción.

![Template 1](../images/template1.png)
![Template 2](../images/tamplate2.png)
![Template 3](../images/tamplete3.png)
![Template 4](../images/template4.png)

La plantilla 4 aloja las mismas piezas que la plantilla 3 pero en una orientación diferente, de tal forma que ambas plantillas permiten el taladrado de agujeros en 2 planos diferentes para cada pieza.

El modelo CAD de estas plantillas esta disponible en este enlace ![](./CAD/Plantillas_Taladrado.f3d), siendo desarrollado mediante el software Fusion360.

El ensamble del armazón (pieza roja y verde) fabricado en aluminio 6061, tiene una masa de alrededor de 70kg, y junto a la geometría de la plantilla y las piezas alojadas, se estima un peso máximo de alrededor de 90Kg.

[Documentación Completa de toda la planta](https://github.com/APM-Kullu/Project/tree/main/PlantaAutomatizada)

<button style="background-color: #4CAF50; /* color de fondo */
               color: white; /* color del texto */
               border: none; /* borde del botón */
               padding: 10px 20px; /* espacio alrededor del texto */
               text-align: center; /* centrar el texto */
               text-decoration: none; /* sin subrayado */
               display: inline-block; /* mostrar en línea */
               font-size: 16px; /* tamaño de la fuente */
               margin: 10px; /* margen externo */
               cursor: pointer; /* cursor de puntero */"
        onclick="window.location.href = window.location.origin + '/kulluWebSite/controladores'">
Ver Los controladores industriales </button>