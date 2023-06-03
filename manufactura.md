---
layout: page
title: Etapas de manufactura 
---

![image](https://github.com/APM-Kullu/Project/assets/52173621/def06eeb-07b0-49a2-8bf6-8774c74c4185)

# Etapas en el proceso de fabricación de piezas de MDF

El proceso de fabricación de piezas de MDF (tablero de fibra de densidad media) incluye varias etapas, desde el corte láser hasta el almacenamiento. En este documento se describirán las diferentes etapas del proceso en el orden en que se realizan.
Las piezas a desarrollar son una estantería de vinos, un taburete y una base para un computador portátil.

## 1. Suministro de láminas de MDF mediante montacargas

(1 operario)
El proceso de suministro de paquetes de láminas de MDF mediante un montacargas implica los siguientes pasos:

1. Preparación del área de carga: antes de que llegue el montacargas con los paquetes de láminas de MDF, se debe preparar el área de carga para recibir la carga. Esto puede incluir la limpieza del área y la colocación de las barreras de seguridad necesarias para proteger a los trabajadores y las instalaciones.

2. Descarga del montacargas: cuando llega el montacargas con los paquetes de láminas de MDF, el conductor debe detener el vehículo en el área de carga y asegurarse de que el freno de mano esté activado. A continuación, se procede a descargar la carga del vehículo.

3. Ubicación de los paquetes: una vez que se han descargado los paquetes de láminas de MDF del montacargas, se deben ubicar en la zona de almacenamiento correspondiente. Esta zona de almacenamiento debe estar previamente designada y organizada para facilitar la ubicación de los paquetes.

4. Verificación de la cantidad y calidad: antes de proceder a utilizar las láminas de MDF en el proceso de fabricación, se debe verificar la cantidad y calidad de los paquetes suministrados. Esto implica contar las láminas y asegurarse de que no estén dañadas o rotas.

5. Transporte de las láminas: una vez que se han verificado los paquetes de láminas de MDF, se procede a transportarlas al área de producción. Esto puede implicar el uso de carretillas elevadoras o equipos de transporte especializados.

6. Las láminas comerciales son muy grandes para entrar en la máquina de corte laser, por lo que estas se deben cortar en 4 partes con una sierra de mesa por parte del operario del área.

Cabe resaltar que el proceso anterior lo realiza un mismo operario y pasa las láminas ya cortadas por un buffer o cinta transportadora, para la siguiente etapa

## 2. Corte láser

(1 operario)
El segundo paso se realiza por un operario que suministra las láminas de MDF en la máquina de corte láser. Para lograr una precisión óptima en el corte, se utiliza un láser de alta precisión que corta las piezas de MDF de acuerdo con las especificaciones de diseño, lo que reduce los residuos y el desperdicio de material.

Para llevar a cabo el corte láser, se realizó una simulación en el software Fusion 360 a partir del plano CAD de todas las piezas. Sin embargo, aún existe incertidumbre en cuanto a la velocidad de corte real de la máquina seleccionada, debido a que los parámetros exactos de la misma no se encuentran disponibles en la página del proveedor. Por lo tanto, se seleccionó un parámetro de potencia y se obtuvo una estimación de la velocidad de corte a través de la web MantechMachinery. La simulación, junto con los planos de corte y el modelo CAD de las tres piezas, se encuentra disponible en el archivo "corteLaser.f3d".

Para llevar a cabo el corte láser se utiliza una lámina de MDF de 1300 mm x 900 mm x 15 mm como entrada, y se obtienen como salida las piezas individuales para armar 1 taburete, 1 portavinos y 2 bases para PC. El tiempo total estimado para este proceso es de 1:29 minutos.

Las lámina a cortar tienen las siguientes medidas: 1200 x 900 mm. La máquina de corte cuenta con una potencia de al menos 150 W.

## 3. Separación de piezas

(1 operario)
El tercer paso en el proceso de fabricación de las piezas de MDF es la separación de las piezas cortadas. Este paso se realiza por un operario que se encarga de retirar las piezas cortadas del tablero principal y clasificarlas según su tamaño.

El operario toma las piezas cortadas y las separa en dos grupos, uno para las piezas grandes y otro para las piezas pequeñas. Cada grupo se introduce en su respectivo buffer para pasar al siguiente paso en el proceso de fabricación, que es el área de fresado.

Es importante destacar que la separación de las piezas según su tamaño es un paso crítico para asegurar la eficiencia. Toma Al rededor de 1:30 minutos por placa que entrega la máquina de corte. Además, la separación de las piezas grandes y pequeñas permite un mejor control de la producción y una organización más eficiente del flujo de trabajo.

## 4. Fresado

(2 operario)
Después de separar las piezas, se realiza el fresado. Este proceso implica dar forma a las piezas y cortar cualquier exceso de material que pueda haber quedado después del corte láser. El fresado se realiza con una máquina fresadora de esquinas que acciona el operario del área. Luego se separan en un buffer individual por cada pieza.
Este proceso tarda al rededor de 10 minutos y se realiza por 2 operarios

## 5. Taladrado

(2 operario)
El proceso de taladrado comienza después de que las piezas se han separado por tamaño, han pasado por el proceso de fresado y se han introducido en dos buffers diferentes. El operario comienza por hacer agujeros en las piezas según las especificaciones de diseño utilizando una máquina taladradora de banco y una máquina taladradora con sierra de copa, según los requerimientos de cada pieza.

Una vez que se han taladrado todas las piezas, el operario las pasa por una banda transportadora para el sellado por aerosol. En este punto, el operario debe usar un compresor para limpiar la pieza de viruta antes de proceder con el sellado.

Para realizar el taladrado en MDF, se necesita un taladro de banco de nivel industrial (sobremesa o pie), ya que se requerirá una alta intensidad de uso. Por lo general, para perforar MDF no se necesita una gran potencia de taladro, y un taladro con una potencia de 500 a 700 Watts debería ser suficiente para perforar MDF con brocas para madera estándar. Es importante utilizar la broca adecuada, y para MDF se recomienda una broca para madera con una punta de centrado y una geometría de corte que permita una perforación limpia. Además, es recomendable utilizar un taladro con una broca de punta de carburo, ya que son más duras y resistentes que las brocas de acero de alta velocidad y pueden perforar materiales más duros sin desgastarse rápidamente.

Para esta etapa del proceso se ha seleccionado el taladro de columna B 24 H (400V), y se estima que el proceso de taladrado con dos operarios tomará alrededor de 6 minutos y 30 segundos en completarse.

## 6. Sellado por aerosol

(1 operario)
Una vez que se han cortado, separado, fresado y taladrado las piezas de MDF, se procede al sellado por aerosol. Este proceso implica aplicar una capa de sellador de aerosol sobre las piezas. El sellador ayuda a proteger la superficie de la pieza.

El tiempo que se requiere para realizar el sellado por aerosol de cada pieza depende del tamaño de las mismas, pero en promedio se estima que toma alrededor de 1 minuto por pieza. Una vez que se ha aplicado el sellador, después, un operario pone a secar las piezas en un almacén por un promedio de 4 horas, para asegurar que el sellante quede bien aplicado.

## 7. Ensamble

(2 -3 operarios)
El siguiente paso es el ensamblaje de las piezas. Este proceso implica unir las diferentes piezas según el diseño, para esto, un operario las separa por el tipo de producto (Estantería, taburete y base) y entre 2 o 3 operarios (Dependiendo del volumen de producción), se realiza en ensamblaje del producto por medio de tornillería, al cual para perforar agujeros de 4.2 mm de diámetro en las piezas de MDF, se requieren tornillos para madera de calibre 8. La mayoría de los tornillos necesarios son de 8 x 2", pero para algunas piezas se necesitarán tornillos de 8 x 1-¼". Los proovedores nacionales (Ver sección Tornillos de Equipos) venden los tornillos necesarios para este proceso, y el precio de cada paquete de 100 unidades es de COP 9.800 para los tornillos de 8 x 2" y COP 6.800 para los tornillos de 8 x 1-¼". El costo total dependerá de la cantidad de piezas que se realicen por día. Cabe destacar que estos precios corresponden a una compra nacional de los tornillos.

## 8. Lacado

(1 operario)
Después del ensamblaje, se procede al lacado de las piezas. Este proceso implica aplicar una capa de laca sobre las piezas. La laca ayuda a proteger la superficie de la pieza y a darle un acabado suave y brillante. El lacado se realiza con una pistola de pintura y puede requerir varias capas, dependiendo del diseño y del acabado deseado.

## 9. Almacenaje

(1 operario)
Una vez que se han lacado todas las piezas, se procede al almacenamiento.
Primero se almacenan en un almacén de secado, donde las piezas deben permanecer un tiempo estipulado, para asegurar que el lacado se fijó correctamente, luego se almacenan en un almacén de despacho, donde se surten a los transportistas para la entrega al cliente final.
El almacenamiento adecuado ayuda a proteger las piezas de la humedad y del polvo, lo que puede dañar la superficie.

[Más información sobre la planta](https://github.com/APM-Kullu/Project/tree/main/PlantaManual)

[Articulo completo](https://github.com/APM-Kullu/Project/blob/main/Especificaciones%20de%20Proyecto.pdf)

# Equipos y Herramientas de planta no automatizada

## Materia prima (Lámina de MDF 15 mm) 

La materia prima es una lámina de MDF de 15 mm de espesor y de dimensiones 1.8 m x 2.4 m. La referencia de la lámina es [Lámina de MDF](https://colombia.masisa.com/producto/mdf/).

<img src="https://i.ebayimg.com/images/g/pq0AAOSwDWVgEWoS/s-l1600.jpg" width="400">

Las láminas son vendidas por Masisa  Colombia, hace falta una cotización al por mayor (Cuantas).

<!-- -------------------------------------------------------------------------------------------------------------------------------------------------------- -->
## Corte previo de lámina 

Para cortar MDF se requiere de una sierra industrial, en este caso se hará una estación de corte con una sierra circular de mano. Se puede utilizar una sierra circular con una potencia mínima de 1200W y una velocidad de al menos 4500 RPM. Sin embargo, es importante tener en cuenta que la capacidad de corte (15 mm) también dependerá del diámetro de la hoja de sierra, la calidad y el tipo de la hoja de sierra, así como de la velocidad de alimentación del material. En general, se recomienda utilizar una hoja de sierra con un número de dientes adecuado para cortar MDF, que puede variar de 40 a 80 dientes. También es importante asegurarse de que la hoja de sierra esté afilada y en buen estado para garantizar un corte limpio y preciso.

Para esta etapa se escogió la maquina [Sierra Circular 7-1/4-pulg 1500W 6000RPM GKS 150](https://homecenterco.scene7.com/is/image/SodimacCO/358623_1?fmt=jpg&fit=fit,1&wid=420&hei=420).

<img src="https://homecenterco.scene7.com/is/image/SodimacCO/358623_1?fmt=jpg&fit=fit,1&wid=420&hei=420" width="400">

La máquina ruteadora es vendida por Homecenter, al ser una compra nacional solo se tiene en cuenta el precio mismo de la máquina: **COP 649.900**.  

<!-- -------------------------------------------------------------------------------------------------------------------------------------------------------- -->
## Corte láser

Para elegir la máquina de corte láser adecuada, es necesario conocer las dimensiones de la lámina a cortar (**1200 x 900 mm**) y en base a ellas, seleccionar el área 
de trabajo necesaria en la máquina. Otro criterio importante a considerar es la potencia de la máquina, ya que esto determina la profundidad de corte. En este caso, 
se requieren cortes de al menos 15 milímetros de profundidad, lo que implica la necesidad de una máquina de corte con una potencia de al menos **150 Watts**.

Para esta etapa se escogió esta [máquina de corte laser](https://es.made-in-china.com/co_starmacnc/product_Over-15mm-Thickness-MDF-Wood-Acrylic-Cutting-Laser-Cutting-Machine-with-150W_eguhionyy.html).

<img src="https://image.made-in-china.com/43f34j00qwlTPuGIvWzD/Over-15mm-Thickness-MDF-Wood-Acrylic-Cutting-Laser-Cutting-Machine-with-150W.webp" width="400">

El precio FOB (Free on Board) está entre **USD 5.200-6.000** dependiendo del tamaño de la máquina. 
(Precio concreto pendiente)

<!-- -------------------------------------------------------------------------------------------------------------------------------------------------------- -->
## Taladrado

Para realizar perforaciones en MDF, es necesario contar con un taladro de banco de nivel industrial (sobremesa o pie), ya que se requerirá una alta intensidad de uso. 
Generalmente, para perforar MDF no se necesita una gran potencia de taladro. Un taladro con una potencia de **500 a 700 Watts** debería ser suficiente para perforar MDF 
con brocas para madera estándar. Lo más importante es usar la broca adecuada. Para MDF, se recomienda una broca para madera con una punta de centrado y una geometría 
de corte que permita una perforación limpia. Se recomienda utilizar un taladro con una broca de punta de carburo, ya que son más duras y resistentes que las brocas de 
acero de alta velocidad y pueden perforar materiales más duros sin desgastarse rápidamente. Además, para perforar MDF no es necesario un taladro con transmisión de 
engranajes, ya que un taladro con transmisión de correa puede ser suficiente y su mantenimiento es más sencillo.

Para esta etapa se escogió el [Taladro de columna B 24 H (400V)](https://www.aslak.es/metal/3020243-taladro-de-columna-b-24-h-400v.html).

<img src="https://www.toolnation.com/media/catalog/product/cache/2b5ad9b52c405c83df66a3873c580358/7/1/1671192/719072/optidrill-b24h-bench-drill-850-watt.jpg" width="400">

El precio FOB (Free on Board) es **EUR 1.759**.

<!-- -------------------------------------------------------------------------------------------------------------------------------------------------------- -->
## Acabado

Para realizar el acabado se usará una maquina ruteadora portatil de tipo industrial:
[Ruteadora Industrial 1800w 2.4hp 15amp](https://www.homecenter.com.co/homecenter-co/product/336547/ruteadora-industrial-24hp-1800w-15amp-vv/336547/).

<img src="https://homecenterco.scene7.com/is/image/SodimacCO/336547_1?fmt=jpg&fit=fit,1&wid=420&hei=420" width="400">

La máquina ruteadora es vendida por Homecenter, al ser una compra nacional solo se tiene en cuenta el precio mismo de la máquina: **COP 535.900**.  

<!-- -------------------------------------------------------------------------------------------------------------------------------------------------------- -->
## Tornillos

Para agujeros de 4.2 mm de diámetro se necesitan tornillos para madera de calibre 8, en su mayoría serán 8 x 2”, pero hay unas excepciones y se usarán 8 x 1-¼”

- [Tornillo Aglomerado Autoperforante 8X2](https://www.homecenter.com.co/homecenter-co/product/86579/tornillo-aglomerado-autoperforante-8x2-100un/86579/).

- [Tornillo Aglomerado Autoperforante 8X1-1/4](https://www.homecenter.com.co/homecenter-co/product/86575/tornillo-aglomerado-autoperforante-8x1-1-4-100un/86575/).

Los tornillos necesarios son vendidos por Homecenter, al ser una compra nacional solo se tiene en cuenta el precio mismo de los tornillos, para saber el costo total
sería necesario conocer la cantidad de piezas que se realizarán por día, los precios por paquetes de 100 unidades son **COP 9.800** y **COP 6800** respectivamente.

(Hace falta cotizar tornillos al por mayor)

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
        onclick="window.location.href = window.location.origin + '/kulluWebSite/planta'">
Ver La planta automatizada </button>