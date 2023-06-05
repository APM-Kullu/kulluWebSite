---
layout: page
title: Equipo Kullu 
---

Nuestro equipo está conformado por estudiantes de último semestre de Ingeniería Mecatrónica de la Universidad Nacional de Colombia

| Julián Camilo Velandia  | Juan Camilo Santana |
| ------------- | ------------- |
| ![WhatsApp Image 2023-03-25 at 9 56 15 AM](https://user-images.githubusercontent.com/52173621/227725140-a133486f-54ae-4367-afb9-ee25b1cfa248.jpeg) | ![WhatsApp Image 2023-03-24 at 1 23 09 PM](https://user-images.githubusercontent.com/52173621/227725124-f4e1b414-601f-4a36-a2a7-1e57248fd6f4.jpeg)  | 
| jvelandiag@unal.edu.co | jsantanas@unal.edu.co   | 
| Camilo Andres Vera | Santiago Hernández |
|------------- | ------------- |
| ![image](https://user-images.githubusercontent.com/52173621/227725131-2239981e-ee9e-4083-a1d6-9d19490631a0.png)  | ![WhatsApp Image 2023-03-24 at 1 34 47 PM](https://user-images.githubusercontent.com/52173621/227725127-9d071e5d-e85c-4cfb-bb2b-622fe6dce57b.jpeg) |
| caverar@unal.edu.co  | shernandezl@unal.edu.co |


# Profesores


| Fábrica Digital  | Robótica Industrial | PLC / SCADA | 
| ------------- | ------------- |------------- |
| ![Ubaldo Garcia](https://user-images.githubusercontent.com/27815265/216997972-edf3994e-d436-4bb1-9ecf-6ddbbb119781.png) | ![PedroCardenas2](https://user-images.githubusercontent.com/27815265/217002716-82745421-6795-466e-a07c-8dbf71520966.png)  | ![Victor Hugo](https://user-images.githubusercontent.com/27815265/217003744-17c4bcf8-e3cb-498e-9021-bb54fbcfe1c8.png)  | 
| Ubaldo Garcia Zaragoza | Pedro F. Cardenas | Victor Hugo Grisales |
| Ingeniero Mecánico  MSc Sistemas Ciberfísicos | Ingeniero Electrónico PhD | Ingeniero Electrónico PhD|
| ugarciaz@unal.edu.co | pfcardenash@unal.edu.co   | vhgrisalesp@unal.edu.co  |

| Industria 4.0  | Protocolos | Gestión de Proyectos  | 
| ------------- | ------------- |------------- |
| ![Eduardo Barrera](https://user-images.githubusercontent.com/27815265/217004618-5ccce037-7ae5-4051-8855-d8abe2f6786f.png) | ![Ricardo Ramirez](https://user-images.githubusercontent.com/27815265/217006274-2eb7f901-a004-4b2e-90cb-3b28883f1837.png)  | ![Luis Miguel 2](https://user-images.githubusercontent.com/27815265/217038088-b323c9fc-63b2-4bba-b678-9b2d02092b11.png) | 
| Eduardo Barrera G.  | Ricardo Ramirez H.   | Luis Miguel Mendez |
| Ingeniero Electrónico MSc| Ingeniero Electrónico PhD | Ingeniero Mecánico PhD|
| ebarrerag@unal.edu.co  | reramirezh@unal.edu.co  | lmmendezm@unal.edu.co  |

# Proceso personal

## Julián Camilo Velandia

### Funciones y Aportes
•	Diseño CAD de la repisa de vinos
•	Selección del robot de la celda robotizada
•	Selección del gripper de la celda robotizada
•	Programación de 8 rutinas del robot de FANUC en Roboguide
•	Ajuste de una rutina global que se maneje por medio de señales de entrada y salida en Roboguide
•	Comunicación de Roboguide con Kepserver medialte opc y señales DDE
•	Simulación de la celda Robotizada
•	Documentación de la celda Robotizada
•	Programación, actualización y mantenimiento de la página web

### Dificultades:
•	Por falta de experiencia en el software Roboguide, se presentaron algunas dificultades que se solucionaron con foros y tutoriales.

### Recomendaciones:
•   En Roboguide, no activar y desactivar elementos decorativos (En nuestro caso mesas y templates) por medio de señales que luego se utilicen en la comunicación de los otros componentes, porque presenta errores
•	Agregar varios puntos intermedios en las rutinas de Roboguide, ya que se presentaban muchas singularidades
•	No simular ventosas en Roboguide, ya que aporta muy poco (Porque el accionamiento de la ventosa funciona por medio de una señal ON/OFF) y presenta Bugs y errores con la rutina
•	Conocer a profundidad el software de Roboguide antes de comenzar a desarrollar, ya que es poco intuitivo




## Camilo Andres Vera

### Funciones y Aportes
•	Delegación de responsabilidades al resto de integrantes del equipo
•	Diseño CAD de una de las piezas a manufacturar y corrección de todos los diseños para su adaptación al procesos de manufactura
•	Diseño global  de la planta no automatizada
•	Diseño global de planta automatizada
•	Simulaciones de corte laser y corte CNC en Fusion360 para estimación de tiempos de manufactura de etapas de la planta automatizada y la planta no automatizada
•	Selección de Fresadora CNC y cinta transportadora
•	Diseño CAD de Plantilla de transporte de piezas
•	Diseño CAD y selección de partes del mecanismo de taladrado, incluyendo los actuadores mecánicos, y el Frame que sostiene el mecanismo, exceptuando la selección de motores.
•	Diseño CAD y selección de partes del mecanismo de mordaza neumática incluyendo la selección de cilindros neumáticos.
•	Diseño CAD a detalle de la planta automatizada
•	Configuración de simulación en NX Mechatronic Concept Designer
•	Programación Ladder en Studio5000 de todas las rutinas que ejecuta el PLC
•	Comunicación OPC UA Entre Rslinx, PLC/LogixEmulate, en NX Mechatronic Concept Designer, e Ignition

### Dificultades:
•	La organización apropiada del proyecto, y la coordinación de responsabilidades, lo que dio como resultado un proceso deficiente en la documentación del proyecto.
•	La imprecisión del motor de físicas de NX, requirió una gran cantidad de tiempo en la iteración de diferentes elementos, tales como la separación de las mordazas, las guías en los bordes de la cinta transportadora, además se tuvieron que modificar los parámetros reales de algunos elementos, como la presión de las válvulas de los cilindros, o el peso real de las plantillas de transporte de piezas, con el fin de poder reflejar una simulación mas real, y evitar situaciones que no reflejan la realidad, tales como el descarrilamiento espontaneo de piezas de la cinta transportadora, o el movimiento de piezas sin motivo alguno, situaciones que solo pudieron ser mitigadas, mas no resueltas por completo.
•	Las latencias en la comunicación entre los servidores de Ignition, implicaron la adición de retardos, con el fin de evitar errores en las señales de las secuencias del proceso.
•	Problemas en la configuración apropiada del control de movimiento en Ladder, debido a la falta de experiencia en el desarrollo del control de servosistemas desde cero en Studio5000.

### Recomendaciones:
•	Simplificar en la medida de los posible, los elementos presentes en la simulación de NX, con el fin de reducir el tiempo de debug de la simulación.
•	No simular Cintas transportadores con curvas en NX, es preferible usar un transmitter, para transportar la pieza de un lugar a otro, o crear un nueva pieza a la salida de la curva y eliminar la pieza que llega a la curva, usando un sensor de colisión, dado que el movimiento en las curvas y las colisiones con los bordes de la cinta transportadora, pueden llevar a situaciones impredecibles como el detenimiento, descarrilamiento, o salto espontaneo de la pieza transportada.
•	No utilizar los objetos de cilindros neumáticos y válvulas dentro de NX, es preferible usar actuadores lineales debido a que se pueden presentar errores en la simulación de la presión de las válvulas, para poder controlar los actuadores lineales con una señal booleana al igual que los cilindros neumáticos, se pueden utilizar adaptadores de señal que permiten controlar variables por medio de condicionales dentro de NX.
•	Es preferible simular los perfiles de movimiento desde Studio5000, ajustando aceleraciones y velocidades máximas, y solo mandar señales de posición desde el PLC/ LogixEmulate a NX, de esta manera se puede lograr un muy buena simulación de un perfil de movimiento trapezoidal, y se pueden evitar problemas relacionados con la baja velocidad de la comunicación OPC UA, que no permite ejecutar el perfil de velocidad de forma precisa desde el PLC. 
