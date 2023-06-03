# Planta automatizada

## Planta completa

<img width="676" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/720cabd6-a22f-4ab4-8a29-0c245d9ec3bf">

La propuesta de automatización consta de la estación de trabajo de la CNC, del brazo Robótico, de la banda transportadora en ciclo y del taladrado. 

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