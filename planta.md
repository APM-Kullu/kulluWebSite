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

Teniendo en cuenta que las laminas de MDF que ingresan a la fresadora CNC deben tener un ancho exacto de 24 pulgadas (609.60mm) y ademas deben contener las piezas cortadas mediante laser sin que que se desprendan completamente de la lamina, se debe modificar el plano de corte laser. A continuación se muestra una imagen donde se muestran las piezas resultantes de dicho corte, de tal forma que todas las piezas se encuentran separadas en dos tableros de 609.80mm x 1050mm.


![image](https://github.com/APM-Kullu/Project/assets/52173621/725c36a6-8580-40b4-8f6b-ce2d9b141833)

Como se muestra en la imagen, las piezas se encuentran unidas al tablero mediante pequeñas conexiones, de tal forma que en la mayoría del proceso de fresado CNC, solo se realice una operación de acabado de bordes, y no un desbaste completo de la pieza.


Mediante Fusion 360 se simulan las operaciones de corte, con una velocidad de corte de 1500mm/min, y una potencia de 200w (Ambos valores sacados de esta [referencia](https://artizono.com/co2-laser-cutting-thickness-speed-chart/)).


![image](https://github.com/APM-Kullu/Project/assets/52173621/90dd41bf-8838-44ff-9771-3c0bfd7101ed)

Se obtienen un tiempo de corte de 11 minutos, 6 segundos para la primera lamina, y 11 minutos, 50 segundos para la segunda lamina.



# Corte CNC

El corte ejecutado por la fresadora CNC se trata de un contoneado de acabado de bordes, ademas del desbaste de los conectores de la pieza con el taladro, repasando el borde de cada pieza en 2mm-3mm en función de su tamaño. La referencia de fresa seleccionada es la [Router Bit for Wood, Particleboard, Plywood Uncoated High-Speed Steel, 3/16" Cutting Diameter, 5/8" Length of Cut](https://www.mcmaster.com/2891A11) de la web de McMASTER-CARR.

Se calcula una velocidad de corte $V_c = 270 \frac{m}{min}$,  con un avance de $V_f = 5760 \frac{mm}{min}$ a 18000 RPM, para metros que se utilizan para simular el corte y obtener los tiempos de corte.

![image](https://github.com/APM-Kullu/Project/assets/52173621/6b0b93ff-db0f-4d24-97b7-97af746b1a5b)

- Tiempo de corte tablero 1: 1 minuto 42 segundos
- Tiempo de corte tablero 2: 1 minuto 53 segundos

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

# Mecanismo de Taladrado

<img width="450" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/8a926470-1f7e-480d-bf90-04f5a03dad38">

![image](https://github.com/APM-Kullu/Project/assets/52173621/403dc967-5dfb-4e68-8105-d3b7c6deb969)


Se trata de un servomecanismo de 3 ejes tipo gantry, que permite taladrar las piezas mediante una broca. Su armazón esta construido mediante extrusiones de aluminio 6060, ángulos de sujeción y tornillos M12 x 60mm.

Esta pensado para ser utilizado junto a un par de mecanismos de mordazas neumáticas las cuales aseguran la posición de las piezas que requieren se taladradas, en un conjunto como el que se presenta en la siguiente imagen.

![image](https://github.com/APM-Kullu/Project/assets/52173621/5cf260e2-2c90-4239-82df-c0240e680afa)

El Eje Y en color azul, es doble, tiene un rango de de 600mm, y es sobre el cual reposa todo el gantry. El eje X se muestra en color amarillo, tiene un rango de 500mm pero se reduce a 450mm debido a los elementos del ensamble. El eje z en color naranja tiene un rango de 400mm y carga consigo un motor con husillo que permite el movimiento de la broca. Cada eje se trata de un mecanismo de tornillo de avance que se adquiere ya ensamblado, y que se controla mediante motores de geometría NEMA 23. Los ejes X y Y se encuentran conectados mediante piezas de aluminio disponibles comercialmente, mientras que la union entre el eje X y el eje Z, asi como la union entre el eje Z y el motor de taladrado, son piezas personalizadas que pueden ser manufacturadas en un aluminio convencional 6061, mediante una fresadora vertical.


## Componentes

- Eje y: 2x [Motor-Mount Positioning Slide for NEMA 23 Motor Frame Size, 600 mm Stroke Length](https://www.mcmaster.com/6734K818)
- Eje X: [Motor-Mount Positioning Slide for NEMA 23 Motor Frame Size, 500 mm Stroke Length](https://www.mcmaster.com/6734K817)
- Eje Z: [Motor-Mount Positioning Slide for NEMA 23 Motor Frame Size, 400 mm Stroke Length](https://www.mcmaster.com/6734K816)
- Conexión entre Eje X y eje Y: 2x [Side Orientation Two-Axis Mounting Plate for Motor-Mount Positioning Slide](https://www.mcmaster.com/6734K821)
- Motor de taladrado: [1.5KW Air Cooled Spindle Square CNC Spindle Motor ER11/ER16](https://www.zhonghuajiangspindle.com/1.5kw-cnc-square-air-cooled-spindle-motor.html)
- Variador de frecuencia para el motor de taladrado: [CIMR-PU2A0018FAA YASKAWA](https://co.wiautomation.com/yaskawa/variadores-motores-proteccion-de-circuitos/CIMRPU2A0018FAA)
- 16x Tornillos M4 x 0.7mm para el fijado entre ejes
- 8x Tornillos M8 x 30mm para el fijado del motor de taladrado.
- 36x [T-Slotted Framing Silver Corner Bracket for 60mm High Rail, 1-1/8" Long](https://www.mcmaster.com/5537T941)
- 144x Tornillos M6 x 20mm para el fijado del armazón de aluminio mediante esquineros
- 10.5 metros de extrusion de aluminio 6060: 2x [T-Slotted Framing Quad Rail, Silver, 60 mm High x 60 mm Wide, Hollow](https://www.mcmaster.com/5537T99-5537T806/)


Para mas detalle sobre la selección de motores y sus respectivos drivers consulte este [documento](./Drivers%20y%20Motores%20(Motion%20Control).md)

El modelo CAD del mecanismo esta disponible en el [archivo](./CAD/MecanismoTaladrado%20v33.f3z)





# Simulaciones de Corte

En este [documento](./PiezasYCortes.md) se describen algunos detalles que se deben tener en cuenta en el proceso de corte, como la modificación de los planos de corte, asi como la velocidad de corte y la simulación de estos procesos.

# Diseño a detalle de planta automatizada

En la siguiente imagen se muestra el diseño CAD de toda la planta automatizada, el cual es utilizado para la simulación mediante el software NX Mechatronics  Concept Designer. Se aclara que el robot que se muestra en el ensamble es de carácter representativo.

![image](https://github.com/APM-Kullu/Project/assets/52173621/2221483e-d8c5-43f3-93ae-f869d127a10c)

La planta ocupa una area de aproximadamente 10.5m x 9.5m, ocupados principalmente por 3 cintas transportadoras, una fresadora CNC, y un robot antropomórfico.

Los componentes comerciales que se utilizaron para el diseño de la planta automatizada, omitiendo los individuales de cada mecanismo son los siguientes:

La maquina CNC seleccionada es la que se muestra en la siguiente imagen, disponible [aquí](https://cntmotion.com/solutions/application/feed-through-parts-machining/)

![image](https://github.com/APM-Kullu/Project/assets/52173621/592b30e0-61f6-4aad-bafd-9c826bfcc713)

- Se utilizan 3 cintas transportadoras como la que se muestra a continuación, disponible en este [enlace](https://www.grainger.com/product/BESTFLEX-Powered-Roller-Conveyor-24-5YDF4?opr=PDPRRDSP&analytics=dsrrItems_5YDF3), cada una de una longitud de 24 pies (aproximadamente 7.3m) y un ancho de 24 pulgadas (61cm).

![image](https://github.com/APM-Kullu/Project/assets/52173621/28bbbb7a-848e-4eb7-aba8-03cc143ffbde)

- Para cada cinta transportadora, se utiliza un sensor para detectar la llegada de una pieza, la referencia seleccionada se encuentra disponible [aquí](https://www.mcmaster.com/7674K812/).

- PLC [1769-L30ER ALLEN-BRADLEY](https://co.wiautomation.com/allen-bradley/plc-sistemas/compactlogix/1769L30ER?gclid=Cj0KCQjw7PCjBhDwARIsANo7CgmpGsCVsYg1hpT3X5nnFjPaax9bad99TBPo--CAxjIbJZAdXeUibbYaAoEbEALw_wcB) con sus correspondientes modulos de entradas y salidas digitales, [1756-IV32 ALLEN-BRADLEY](https://co.wiautomation.com/allen-bradley/modulos/controllogix/1756IV32). y [1756-OV32E ALLEN-BRADLEY](https://co.wiautomation.com/allen-bradley/modulos/controllogix/1756OV32E).

![image](https://github.com/APM-Kullu/Project/assets/52173621/6759657c-c57c-4ff9-94c1-a64dac39382d)



# Plantillas de sujeción de piezas

Las plantillas se proponen como un ensamble de platinas de aluminio de 50mm de espesor, con perforaciones de 8mm de diámetro, para permitir el paso de tornillos M8 de 100 mm de largo, de tal forma que el armazón completo se puede ensamblar usando 96 de estos tornillos. En las dos imágenes que se muestran a continuación se observan las dos partes principales del armazón, donde la parte roja sirve como sostén para toda la plantilla, y ademas cuenta con agujeros diseñados específicamente para el autocentrado de la plantilla con la mordaza neumática, y la parte verde es la que sostiene la geometría de la plantilla donde se alojan las piezas. Todas las platinas fueron diseñadas teniendo en cuenta que se puedan manufacturar en una fresadora vertical convencional de ejes y asi facilitar su producción y remplazo en el mercado local.

![image](https://github.com/APM-Kullu/Project/assets/52173621/ecc41d0c-b92d-4083-b631-0993c545a2a6)
![image](https://github.com/APM-Kullu/Project/assets/52173621/03775231-a804-4f69-88b5-c5215b30d90f)

La pieza ensamblada tiene un tamaño total de 850mm x 24 pulgadas (609.6mm) acorde con el ancho de la cinta transportadora.

Por otro lado se diseñaron 4 geometrías en madera de MDF de 30mm, las cuales pueden ser ensambladas mediante el corte de laminas de 15mm, de tal forma que no se requieran capacidades de manufactura adicionales a las que ya cuenta la planta previo a la implementación de las celdas de manufactura automatizada.

A continuación se presentan las 4 geometrías propuestas, junto con las piezas de corte, con el fin de representar la distribución de las piezas durante el proceso de producción.

<img width="417" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/14da1f6c-8aea-47fa-a3ea-add79389d8fc">
<img width="426" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/419b93f0-6041-4982-8a0b-19d3f0f6f42b">
<img width="423" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/7309c81b-559d-432f-935d-20be8a9362ab">
<img width="421" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/afc22413-f79d-4ec3-a8e1-618398b78261">

La plantilla 4 aloja las mismas piezas que la plantilla 3 pero en una orientación diferente, de tal forma que ambas plantillas permiten el taladrado de agujeros en 2 planos diferentes para cada pieza.

El modelo CAD de estas plantillas esta disponible en este enlace [](https://github.com/APM-Kullu/Project/blob/main/PlantaAutomatizada/CAD/Plantillas_Taladrado.f3d), siendo desarrollado mediante el software Fusion360.

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