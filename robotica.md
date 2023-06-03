---
layout: page
title: Celda Robotizada
---

Para nuestra solución, se requiere un brazo robótico que:
1. Recoja las piezas que salen de la cortadora CNC y las oriente e introduzca en unas plantillas que van a pasar al área de taladrado
2. Recoja las piezas ya taladradas de un template y las lleve a una mesa provisional (Buffer) para luego introducirlas a otro template (Para completar el taladrado de toda la pieza)
3. Recoja las piezas ya taladradas de un template y las lleve a una mesa de salida

## Justificación de la selección de un brazo robótico para la celda robótica
Para la tarea de recoger las piezas en MDF recién cortadas y pasarlas a la siguiente celda, se requiere un brazo robótico con un alcance de entre 1.5 y 2 metros y que pueda soportar alrededor de 7 kilos de carga útil. Después de evaluar varias opciones, se ha seleccionado el brazo robótico FANUC ARC Mate 100iD/8L debido a sus características y capacidades.

## Razones de selección
### Capacidad de carga
El FANUC ARC Mate 100iD/8L tiene una capacidad de carga útil de hasta 9 kilos, lo que es suficiente para manejar la carga de 7 kilos requerida para la tarea. Además, esta capacidad de carga adicional proporciona una margen de seguridad y flexibilidad para futuras aplicaciones o cambios en los requisitos de carga.

### Alcance y precisión
El FANUC ARC Mate 100iD/8L tiene un alcance máximo de 2.023 metros, lo que cumple con los requisitos de alcance de la tarea. Además, este brazo robótico cuenta con una precisión de repetición de +/- 0.05 mm, lo que asegura una colocación precisa de las piezas.

### Flexibilidad y programabilidad
El FANUC ARC Mate 100iD/8L tiene una amplia gama de movimientos, lo que permite una mayor flexibilidad en la tarea. También cuenta con una interfaz de programación intuitiva que facilita la programación y personalización de la tarea. Además, la conectividad de red Ethernet integrada facilita la integración del robot en sistemas de control de producción más grandes.

## Comparativa con otros 2 robots similares
Para validar la selección del FANUC ARC Mate 100iD/8L, se comparó con otros dos robots similares en capacidad y alcance: el ABB IRB 2600 y el KUKA KR 6 R900 sixx.

### ABB IRB 2600
El ABB IRB 2600 tiene una capacidad de carga útil de hasta 12 kilos y un alcance máximo de 0.85 metros. Aunque su capacidad de carga cumple con los requisitos, su alcance es insuficiente para la tarea. Además, su precisión de repetición de +/- 0.02 mm es menor que la del FANUC ARC Mate 100iD/8L. 

### KUKA KR 6 R900 sixx
El KUKA KR 6 R900 sixx tiene una capacidad de carga útil de hasta 6 kilos y un alcance máximo de 0.9 metros. Al igual que el ABB IRB 2600, su capacidad de carga es suficiente pero su alcance no cumple con los requisitos de la tarea. Además, su precisión de repetición de +/- 0.03 mm es ligeramente menor que la del FANUC ARC Mate 100iD/8L. En cuanto a la programación, KUKA utiliza el lenguaje de programación KRL, que puede requerir una curva de aprendizaje adicional.

## Metodología de selección

En cuanto a las metodologías de selección de un brazo robótico, hay varias que se pueden utilizar dependiendo de los requisitos y objetivos de la tarea. Algunas de las metodologías comunes son:

1. Análisis de tareas: Evaluar la tarea específica que se realizará con el brazo robótico, determinando el alcance, la precisión y la carga útil requerida.

2. Evaluación de costos: Analizar los costos asociados con la compra, instalación, programación y mantenimiento del brazo robótico, para determinar la mejor opción económica.

3. Evaluación de riesgos: Evaluar los riesgos asociados con la tarea y determinar si el brazo robótico seleccionado puede manejar la tarea de manera segura y eficiente.

4. Análisis de rendimiento: Evaluar el rendimiento del brazo robótico en términos de velocidad, precisión y capacidad de carga, para determinar si el robot es capaz de cumplir con los requisitos de la tarea.

5. Evaluación de la compatibilidad del sistema: Evaluar la capacidad del brazo robótico para integrarse con otros sistemas de producción, como sensores y software de control.

6. Análisis de flexibilidad: Evaluar la capacidad del brazo robótico para manejar diferentes tareas y adaptarse a cambios en los requisitos de la tarea en el futuro.

Estas metodologías pueden ser combinadas y adaptadas según sea necesario para ayudar en la selección del brazo robótico adecuado para una tarea específica.

<img width="192" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/3dd9d23f-8887-41b0-8325-c0e3cdeeb141">

[Más información](https://www.fanuc.eu/uk/en/robots/robot-filter-page/m-10-series/m-10id-8l)

# Selección de una pinza por vacío para agarrar las piezas cortadas de MDF
Para cumplir con la tarea de recoger las piezas de MDF recién cortadas y colocarlas en la siguiente celda, se requiere una pinza por vacío compatible con el brazo robótico de FANUC. La pinza por vacío debe tener la capacidad de agarrar piezas de MDF con un grosor de 15 mm y para las piezas más grandes, con un radio de 45 cm.

Después de evaluar varias opciones, se ha seleccionado la pinza por vacío VGC10 del fabricante On Robot debido a sus características y capacidades.

# Razones de selección
## Capacidad de carga
La pinza por vacío eléctrica VGC10 tiene posibilidades de personalización ilimitadas. También tiene ventosas intercambiables para casi cualquier necesidad de aplicación y Puede levantar objetos de hasta 15 kg.

## Flexibilidad y programabilidad
La pinza por vacío eléctrica VGC10 es compatible con el brazo robótico de FANUC, lo que asegura una fácil integración y compatibilidad. También cuenta con una interfaz de programación intuitiva que facilita la programación y personalización de la tarea. Además, la conectividad de red Ethernet integrada facilita la integración del gripper en sistemas de control de producción más grandes.

![image](https://github.com/APM-Kullu/Project/assets/52173621/453066fd-ad10-478f-8d2b-e85fea9e3be1)

[Más información](https://www.roscomponents.com/es/pinzas/292--vgc10-.html)

# Simulación Pick and Place en Roboguide

[![Alt text](https://img.youtube.com/vi/rG_TBuvx13Y/0.jpg)](https://www.youtube.com/watch?v=rG_TBuvx13Y)

Los templates donde se organizan las piezas son los siguientes

### Template 1
<img width="417" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/14da1f6c-8aea-47fa-a3ea-add79389d8fc">

### Template 2
<img width="426" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/419b93f0-6041-4982-8a0b-19d3f0f6f42b">

### Template 3
<img width="423" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/7309c81b-559d-432f-935d-20be8a9362ab">

### Template 4
<img width="421" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/afc22413-f79d-4ec3-a8e1-618398b78261">


El flujo de la celda es el siguiente

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
        onclick="window.location.href = window.location.origin + '/kulluWebSite/robotica'">

Ver Celda robotizada </button>