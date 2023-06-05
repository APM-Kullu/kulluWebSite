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

<img width="750" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/538ce18f-271a-49c2-83ae-2b68c19d94ec">

# Medidas de seguridad en la celda robótica
Es importante tomar medidas de seguridad en la celda robótica para garantizar la seguridad de los trabajadores y el correcto funcionamiento del brazo robótico. A continuación, se describen algunas medidas de seguridad recomendadas para esta celda.

1. Protección de la zona de trabajo
Se debe instalar una barrera de seguridad alrededor de la zona de trabajo para evitar que los trabajadores ingresen accidentalmente en la zona de operación del robot. También se pueden utilizar sensores de presencia para detener el robot en caso de que un trabajador entre en la zona de trabajo.

2. Botón de parada de emergencia
Se debe instalar un botón de parada de emergencia cerca de la zona de trabajo para que los trabajadores puedan detener el robot en caso de una emergencia.

3. Protección del cableado y la alimentación
El cableado y la alimentación del robot deben estar protegidos para evitar cortocircuitos y otros problemas eléctricos. Se pueden utilizar canalizaciones y cubiertas de protección para evitar el acceso no autorizado a los componentes eléctricos.

4. Capacitación de los trabajadores
Es importante capacitar a los trabajadores sobre el funcionamiento y las precauciones de seguridad del brazo robótico. Los trabajadores deben conocer las medidas de seguridad a tomar en caso de emergencia y estar al tanto de los riesgos potenciales de la operación del robot.

5. Mantenimiento regular del robot
El brazo robótico debe recibir un mantenimiento regular para garantizar su correcto funcionamiento y evitar fallos o accidentes. Esto incluye la inspección periódica de los componentes mecánicos y eléctricos, así como la realización de reparaciones y actualizaciones según sea necesario.

6. Cumplimiento de las normativas de seguridad
Es importante asegurarse de cumplir con las normativas de seguridad aplicables en la operación de robots industriales. Esto puede incluir normativas sobre la instalación y uso de robots, así como sobre la capacitación y protección de los trabajadores que operan el robot.

El diagrama muestra la disposición de las medidas de seguridad en la celda robótica. El operador está situado fuera de la celda y tiene acceso a un botón de parada de emergencia (E-Stop) y una luz de seguridad que indica el estado del sistema. Dentro de la celda, el controlador del robot está conectado a las alfombras de seguridad que detectan la presencia del operador y detienen el robot si se produce un error.

![image](https://user-images.githubusercontent.com/52173621/233763296-5de27943-52b3-4837-86e4-dec3e85b6b3c.png)


# Operador
El operador se encuentra fuera de la celda robótica. El operador tiene acceso a un botón de parada de emergencia (E-Stop) y una luz de seguridad que indica el estado del sistema. Estos elementos permiten al operador detener rápidamente el robot en caso de emergencia.

# Robot Controller
Este bloque representa el controlador del robot, que está ubicado dentro de la celda robótica. El controlador se encarga de recibir las órdenes del sistema de control y enviar señales al robot para que realice la tarea programada.

# Robot Controller
Este bloque representa la conexión entre el controlador del robot y las alfombras de seguridad. Las alfombras de seguridad están ubicadas en el suelo de la celda robótica y detectan la presencia del operador. Si el operador entra en la celda robótica, las alfombras de seguridad envían una señal al controlador del robot para detener inmediatamente el movimiento del robot.

# Safety Mats
Este bloque representa las alfombras de seguridad ubicadas en el suelo de la celda robótica. Las alfombras de seguridad detectan la presencia del operador y envían una señal al controlador del robot para detener inmediatamente el movimiento del robot.

# Safety Light
la luz de seguridad está ubicada fuera de la celda robótica. La luz de seguridad indica el estado del sistema y proporciona información al operador sobre el estado del robot y cualquier problema que pueda ocurrir durante la operación.


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
        onclick="window.location.href = window.location.origin + '/kulluWebSite/actuadores'">
Ver Actuadores de automatización </button>