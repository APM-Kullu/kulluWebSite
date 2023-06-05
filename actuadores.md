---
layout: page
title: Actuadores de automatización
---


# Drivers y Motores - Control de Movimiento

Para determinar los servomotores y drivers adecuados que se utilizarán en el sistema de taladrado, es necesario realizar cálculos para determinar el torque requerido en cada eje del mecanismo. Además, consideraremos el uso de carriles lineales para cada eje, lo cual afectará los cálculos de velocidad y aceleración. Es necesario tener en cuenta los carriles de guía lineal del [Mecanismo de taladrado](MecanismoTaladrado.md) ya que estos ponen límites en las cargas, velocidades y aceleraciones.

## Carriles de guía lineal
Distancia por vuelta: 10 mm/rev

**Capacidad:** 395 lbs (179 kg).

**Aceleración máxima:** 0.3 g (2.94 m/s^2)

**Torque máximo:** 176 in-oz (1.243 N-m)

**Velocidad máxima:**
- Eje X: 650 mm/s (3900 RPM)
- Eje Y: 470 mm/s (2820 RPM)
- Eje Z: 790 mm/s (4740 RPM)

## Cargas de cada eje
### Eje Y:
- Mounting plate x2: 3.4 kg
- Motor Eje X: 5 kg
- Carril Eje X: 9 kg
- Motor Eje Z: 5 kg
- Carril Eje X: 8 kg
- Mounting plate: 0.713 kg
- Motor husillo: 4.3 kg
- Broca: 0.01 kg

**TOTAL: 35 kg**
### Eje X:
- Motor Eje Z: 5 kg
- Carril Eje X: 8 kg
- Mounting plate: 0.713 kg
- Motor husillo: 4.3 kg
- Broca: 0.01 kg

**TOTAL: 18 kg**
### Eje Z:
- Motor husillo: 4.3 kg
- Broca: 0.01 kg

**TOTAL: 4.31 kg**

## Cálculo de Torque necesario para cada eje
En primer lugar se fija la aceleración deseada para cada eje, esto teniendo en cuenta el límite de los carriles y las velocidades máximas de cada eje. Luego se hace una simplificación de la carga de cada eje como una masa puntual par realizar el cálculo del torque necesario usando la formula de torque:
$$T_{in}=\frac{F\cdot P}{2000 \pi \cdot \eta }$$

### Eje Y:
Se supone una velocidad máxima de 450 mm/s para que no exceda la capacidad de este carril y un tiempo de aceleración de 0.2 s:

<img src="https://github.com/APM-Kullu/Project/assets/42346345/a36e4887-97ad-4a17-9b55-99fb3cdc6a08" width="500" alt="Imagen escalada">

$a=\frac{450\frac{mm}{s}}{0.2 s}$      $a=2250\frac{mm}{s^2}$      $a=2.25\frac{m}{s^2}$

Ahora el diagrama de cuerpo libre queda: 

<img src="https://github.com/APM-Kullu/Project/assets/42346345/7bfbc5ed-a156-41e6-8bda-eacba0e5138b" width="500" alt="Imagen escalada">

y por último se puede hallar el torque con la fórmula antes mencionada:

$T_{in}=\frac{78.75 N\cdot 10 mm}{2000 \pi \cdot 0.85 }$

**$T=0.147 N-m$**

**$V_{max}=0.45 \frac{m}{s}(2700 RPM)$**

**$a_{max}=2.25 \frac{m}{s^2}$**


### Eje X:
Se supone una velocidad máxima de 600 mm/s para que no exceda la capacidad de este carril y un tiempo de aceleración de 0.25 s:

<img src="https://github.com/APM-Kullu/Project/assets/42346345/d4874cc2-2f0b-462d-8cd5-44dd71883064" width="500" alt="Imagen escalada">

$a=\frac{600\frac{mm}{s}}{0.25 s}$      $a=2400\frac{mm}{s^2}$      $a=2.4\frac{m}{s^2}$

Ahora el diagrama de cuerpo libre queda: 

<img src="https://github.com/APM-Kullu/Project/assets/42346345/ee0e6f8d-2c65-44fc-a10b-8a01bfc0d27d" width="500" alt="Imagen escalada">

y por último se puede hallar el torque con la fórmula antes mencionada:

$T_{in}=\frac{43.2 N\cdot 10 mm}{2000 \pi \cdot 0.85 }$

**$T=0.081 N-m$**

**$V_{max}=0.6 \frac{m}{s}(3600 RPM)$**

**$a_{max}=2.4 \frac{m}{s^2}$**

### Eje Z:
Se supone una velocidad máxima de 600 mm/s para que no exceda la capacidad de este carril y un tiempo de aceleración de 0.25 s:

<img src="https://github.com/APM-Kullu/Project/assets/42346345/d4874cc2-2f0b-462d-8cd5-44dd71883064" width="500" alt="Imagen escalada">

$a=\frac{600\frac{mm}{s}}{0.25 s}$      $a=2400\frac{mm}{s^2}$      $a=2.4\frac{m}{s^2}$

Ahora el diagrama de cuerpo libre, suponiendo el caso más crítico en donde el motor debe acelerar la carga en contra de la gravedad, queda: 

<img src="https://github.com/APM-Kullu/Project/assets/42346345/f3ad51d8-ccac-49de-8f74-1cb3fbc9d024" width="500" alt="Imagen escalada">

y por último se puede hallar el torque con la fórmula antes mencionada:

$T_{in}=\frac{53.63 N\cdot 10 mm}{2000 \pi \cdot 0.85 }$

**$T=0.099 N-m$**

**$V_{max}=0.6 \frac{m}{s}(3600 RPM)$**

**$a_{max}=2.4 \frac{m}{s^2}$**


## Selección de motor y Driver
Para la selección del servomotor que se debe usar fue necesario tener en cuenta el tamaño del marco que requieren los carriles de guía lineal, este debía ser de tamaño NEMA 23, por lo cual se buscó en la familia de los servomotores Kinetix TL/TLY la cual cuenta con el tamaño deseado. El motor que cumple con el torque y velocidad maxima deseados es el de referencia TLY-A220P-BJ64AA el cual es compatible con el driver Kinetix 350


# Sistema Neumático
Este documento presenta el diseño del sistema neumático de la planta automatizada. Este sistema utiliza tecnología neumática para el control y accionamiento 
de diferentes procesos y mecanismos en la planta. El diseño se basa en la utilización de componentes clave como un compresor de aire, válvulas neumáticas, 
cilindros y otros dispositivos neumáticos. Estos componentes trabajan en conjunto con el PLC para proporcionar energía y control a los distintos mecanismos 
automatizados de la planta.


## Diagrama Sistema Neumático
![Diagrama neumatico_page-0001](https://github.com/APM-Kullu/Project/assets/42346345/26222e50-c0c4-49e7-a6ca-bb3b0fb1604f)

## Compresor
Ya que el compresor solo se usará para el sistema de mordazas neumáticas, se escoge un compresor de 2 etapas 5 HP 500L, el cual cumple con la capacidad de flujo
requerida para accionar los cuatro cilindros neumáticos y con la presión requerida. La referencia del compresor es 
[E230ME0500-500](https://www.evans.com.co/producto/compresor-aire-lubricado-2-etapas-5-hp-motor-electrico-tanque-500-litros-175-psi-e230me0500-500/).

<img src="https://sp-ao.shortpixel.ai/client/to_auto,q_glossy,ret_img,w_450,h_450/https://www.evans.com.co/wp-content/uploads/2017/06/Compresores_EVANS_E230ME0500_500_1L_50.jpg" width="400">

MOTOR:

Potencia del motor: 5.00 HP.
Velocidad del Motor: 1750 RPM.
Tipo de motor: Eléctrico.
Marca del motor: Weg/Siemens.
Fases: Trifásico.
Voltaje: 220/440 V.

CARACTERÍSTICAS:

Tipo de compresor: Reciprocante.
Presión máxima: 175 PSI.
PCM @ 90 PSI: 18.30 pcm.
PCM @ 150 PSI: 16.00 pcm.
Capacidad del tanque: 500.00 L.
Posición del tanque: Horizontal.
Ciclo de trabajo: 70% Trabajo - 30% Descanso.
Tiempo de trabajo: 10000 horas.
Acoplamiento del motor a la cabeza: Banda V.
Tipo de guarda: Metálica.
Presentación: Estacionario.

CENTRO DE COMPRESIÓN:

Número de cabezas: 1.
Número de etapas: 2.
Número de cilindros/pistones: 2.
Modelo del Cabezal: CE230.
Aceite recomendado para la cabeza: RC-AW100 (incluido en la compra del compresor).
Capacidad de aceite para la cabeza: 1.50 L.
Primer y segundo cambio de aceite: 25/50 horas (Usar aceite RC-AW100).
Cambios de aceite posteriores: 1500 horas (Usar aceite RC-X3000 vendido por separado).
Potencia mecánica de la cabeza: 5.00 HP.
Desplazamiento: 23.00 pcm.

El precio del compresor es de **COP 12.066.243**. 

## Unidad de Mantenimiento (FRL)

Para la unidad de mantenimiento se escoge una FRL, la cual combina el filtrado, la regulación de presión y la lubricación en un solo dispositivo, 
garantizando un suministro de aire limpio, regulado y lubricado para los sistemas neumáticos, lo que resulta en un rendimiento óptimo, una mayor durabilidad 
de los componentes y una operación confiable. La referencia de la unidad de mantenimiento es [AC20 Series 8492T115](https://www.mcmaster.com/8492T115/).

<img src="https://www.mcmaster.com/mvD/Contents/gfx/ImageCache/849/8492t2-@1x_636987887154604691.png?ver=ImageNotFound">

Serie del fabricante: AC20.
Configuración: En línea.
Tamaño de la tubería: 1/8".
Caudal máximo: 32 scfm a 100 psi.
Presión máxima: 145 psi.
Capacidad de eliminación de partículas: Hasta 5 micrones.
Material del recipiente: Plástico de policarbonato transparente.
Tipo de drenaje: Automático.
Rango de ajuste de presión de salida: 7.25-123 psi.
Capacidad de lubricante: 0.85 oz.
Incluye manómetro.
Altura total: 5 1/2".
Ancho total: 5".
Precisión de regulación: ±3%.

El precio del compresor es de **USD 94.40**.

## Válvulas de Control Direccional

Se han seleccionado válvulas 5/2 con activación por bobina eléctrica y retorno por muelle. Estas válvulas cuentan con dos posiciones de trabajo y cinco conexiones, lo que permite controlar el flujo de aire en el sistema neumático. La activación por bobina eléctrica proporciona un control preciso y rápido de las válvulas, mientras que el retorno por muelle garantiza la seguridad y la fiabilidad de la operación, asegurando que las válvulas vuelvan a su posición original en caso de fallo eléctrico. La referencia de las válvulas es [6425K11](https://www.mcmaster.com/6425K11/).

<img src="https://www.mcmaster.com/mvD/Contents/gfx/ImageCache/642/6425k132-@1x_636881540402220587.png?ver=ImageNotFound">
<img src="https://www.mcmaster.com/mvD/Contents/gfx/ImageCache/c03/c03a-E5l1-digital-master1551986280-p9@1x_636874820347248581.png?ver=ImageNotFound">

Función: Control direccional.
Tipo de válvula: Tipo carrete (spool).
Tipo de válvula de control direccional de aire: 4 vías.
Patrón de flujo: 5/2.
Para tipo de cilindro de aire: Doble efecto.
Actuación: Eléctrica (solenoides).
Retorno de actuación: Por resorte.
Caudal máximo: 56 scfm a 100 psi.
Rango de presión: 15-150 psi.
Rango de temperatura: -10°F a 115°F.
Tipo de conexión de entrada: Roscada.
Tamaño de entrada: 1/8 NPTF.
Tipo de conexión de salida: Roscada.
Tamaño de salida: 1/8 NPTF.
Tipo de conexión de escape: Roscada.
Tamaño de escape: 1/8 NPTF.
Material del cuerpo: Aluminio.
Dimensiones generales:
Longitud: 5 1/2 pulgadas.
Ancho: 7/8 pulgadas.
Altura: 2 3/4 pulgadas.

El precio de la válvula es de **USD 112.92** y se requieren 4.

## Cilindros Neumáticos 

La referencia de los cilindros neumáticos utilizados se encuentra en [60405K127](https://www.mcmaster.com/60405K127/) y se usa en el 
[Mecanismo Mordaza Neumática](MecanismoMordazaNeumatica.md). 

<img src="https://www.mcmaster.com/mvD/Contents/gfx/ImageCache/640/6402t811-1647969487-p9@1x_637835482946000001.png?ver=ImageNotFound">

Tipo de cilindro: Tie Rod (de tipo tirante).
Tamaño del orificio: 32 mm.
Carrera: 275 mm (retraído: 421 mm, extendido: 696 mm).
Fuerza a 50 psi: 63 lbs.
Fuerza a 100 psi: 125 lbs.
Tipo de amortiguación: Amortiguación ajustable.
Tipo de actuación: Doble efecto (aire para extender y aire para retraer).
Material del cuerpo: Aluminio extruido.
Material del émbolo: Acero inoxidable 431.
Diámetro de la varilla: 12 mm.
Tipo de rosca de la varilla: M10.
Tamaño de la entrada de aire: 1/8 (rosca BSPP).

Estas características demuestran que el cilindro neumático seleccionado es adecuado para nuestras necesidades en términos de tamaño, fuerza, capacidad de amortiguación y durabilidad.

El precio del cilindro es **USD 233.28** y se requieren 4.

## Mufflers

Los "mufflers" (también conocidos como silenciadores o atenuadores) son dispositivos utilizados para reducir el ruido generado por el escape de gases en sistemas de aire comprimido. Estos dispositivos se instalan en el sistema de escape o en las salidas de aire y tienen la función de disminuir la intensidad del sonido producido por el flujo de gases. Se utilizan comúnmente en las salidas de aire de las válvulas de control direccional en sistemas neumáticos. Estos dispositivos se instalan en la salida de escape de las válvulas para reducir el ruido generado por el escape de aire comprimido. La referencia escogida es [7352N61](https://www.mcmaster.com/7352N61/).

<img src="https://www.mcmaster.com/mvD/Contents/gfx/ImageCache/735/7352N61multipositive_top_positive_right_washer_1614256045_192@1x_637498313096587939.png?ver=ImageNotFound">

Estilo: A.
Tipo de conexión: Tubo.
Tipo de conexión de tubo: Roscado.
Tamaño de tubo: 1/8".
Tipo de rosca: BSPP (British Standard Pipe Parallel).
Género: Macho.
Caudal máximo: 21 scfm @ 100 psi (Pies cúbicos estándar por minuto a 100 psi).
Presión máxima: 175 psi.
Temperatura máxima: 175° F.
Altura: 1 3/4".
Estilo de accionamiento: Hexagonal externo.
Para uso con: Aire, gas inerte.
Material: Latón.
Construcción del cuerpo: Poroso.
Para reducir: Ruido, partículas.
Remueve partículas de tamaño hasta: 40 micrones.
Calificación de reducción de ruido: 10-20 dB.

El precio de los Mufflers es **USD 4.18** y se requieren 8. 

## Válvulas de control de flujo

La válvula de control de flujo de aire con codo ajustable de precisión. Esta válvula se utiliza en sistemas neumáticos para controlar y regular el flujo de aire en una dirección específica. La función principal de esta válvula es controlar la velocidad y el flujo de aire en un circuito neumático. Será utilizada para regular la velocidad de los cilindros neumáticos. La referencia escogida es [4076K37](https://www.mcmaster.com/4076K37/).

<img src="https://www.mcmaster.com/mvD/Contents/gfx/ImageCache/407/4076k28--885391fc6361560182088-p9@1x_636957609029154304.png?ver=ImageNotFound">

Uso: Aire comprimido.
Función de la válvula: Ajuste de flujo.
Tipo de válvula: Aguja.
Forma: Codo de 90°.
Actuación: Presión.
Control de flujo: En una dirección.
Tipo de control de flujo: Salida del cilindro.
ISO Designación: Meter Out.
Mecanismo de ajuste de flujo: Dial.
Número de puertos: 2 (1 de flujo, 1 de entrada, 1 de salida).
Material del cuerpo: Plástico de nylon.
Material del accesorio: Latón.
Coeficiente de flujo (Cv): 0.006.
Tasa de flujo máxima: 0.1 scfm a 100 psi.
Presión máxima: 145 psi.
Rango de temperatura: 35° a 155° F.
Dimensiones: Longitud de 15/16", ancho de 7/16", altura de 1 5/16".
Conexión de entrada: Roscada (tipo NPT) de 1/8".
Conexión de salida: Push to Connect para tubo de 1/8" de diámetro exterior.

El precio de la válvula es de **USD 22.75** y se requieren 8.



# Mordaza Neumática

![](../images/mordaza1.png)

La mordaza neumática se trata de un mecanismo que permite el movimiento en un eje controlado por un cilindro neumático de doble efecto y soportado por dos guías lineales. Se encarga de la fijación de las plantillas en las estaciones de taladrado e intercambio de piezas, con el fin de garantizar un posicionamiento adecuado tanto en el taladrado, como en el pick an place de las piezas por parte del robot, eliminando la necesidad de un sistema de vision de maquina para el posicionamiento de las piezas.

El sistema fue diseñado teniendo en cuenta su fácil manufactura, por lo cual solo requiere la fabricación de soportes en acero conformado en caliente mediante soldadura, los cuales se representan en colo negro en la imagen presentada anteriormente (sin incluir la parte fija del cilindro neumático), el corte de 6 platinas de aluminio 6061 de 40mm de de espesor, el corte de una barilla de acero de 8mm de diámetro, la impresión 3D en un material de baja fricción como el nylon, de las piezas representadas en color blanco, y el corte de extrusiones de aluminio 8020 y 4020, en las piezas representadas de color naranja.

El cilindro neumático junto con sus sensores de final de carrera, y las guías que soportan la mordaza, fueron seleccionadas del proveedor de partes McMASTER-CARR, teniendo en cuenta que se requiere un movimiento mayor a los 250mm, que es el tamaño de los elementos que ingresan dentro de la plantilla. Las referencias de partes seleccionadas son las siguientes:

- [Enclosed-Body NFPA Tie Rod Air Cylinder - Cushioned, Double Acting, 32mm Bore, 275mm Stroke Length](https://www.mcmaster.com/60405K127/)

![](../images/cilindro.png)

- 2 x [Telescoping Slide - C Rail Profile, 43 mm Wide x 610 mm Long Rail](https://www.mcmaster.com/8379K12/)

![](../images/guia.png)

- 2x [10-30V DC NPN Sensor for 2-1/2" Bores Enclosed-Body NFPA Tie Rod Air Cylinder](https://www.mcmaster.com/6402T924/)

![](../images/sensorCilindro.png)

El cilindro neumático fue seleccionado en base al alcance del movimiento requerido, a partir de allí solo se requirió verificar que la presión maxima que puede entregar el cilindro, fuese mayor a la presión maxima requerida, debida a la fuerza del peso máximo de la carga desplazada, que es de alrededor de 100N, (el peso de los elementos fijos al vástago del cilindro).

Teniendo en cuenta que el diámetro del embolo es de 32mm, y que la presión maxima del cilindro es de 100 psi (0.69 MPa) se tiene que la fuerza maxima que puede entregar el cilindro es de:

$F = 0.69 MPa \times \pi \times 16mm^2 = 554.9 \N$

De lo anterior se concluye que el cilindro cuenta con la fuerza suficiente para mover la carga de 100N, ademas de tener un margen de seguridad aceptable.

Los tornillos requeridos para la construcción de una mordaza, son los siguiente:

- 12x M8  x 15mm cabeza plana
- 4x  M8  x 80mm
- 12x M6  x 30mm cabeza plana
- 4x  M12 x 80mm
- 1x  M12 x 40mm
- 17x M5  x 40mm

El Diseño CAD del mecanismo se encuentra disponible en este [enlace](./CAD/MordazaNeumatica%20v28.f3d).







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
        onclick="window.location.href = window.location.origin + '/kulluWebSite/digital'">
Ver Digital Factory </button>