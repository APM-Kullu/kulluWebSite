---
layout: page
title: Digital Factory
---


Para la simulación de la planta  en un gemelo digital, se utilizo el software Siemens NX Mechatronics Concept Designer para emular el comportamiento físico de todos los sensores y actuadores de la planta, en conjunción con el software RoboGuide de FANUC, para la simulación del movimiento del Robot antropomórfico. 
Dentro de NX se simularon elementos tales como: cilindros neumáticos, electroválvulas, sensores de detección de pieza, cintas transportadoras con trayectorias curvas, ejes de movimiento lineal servocontrolados, y algunas de las colisiones allí presentes, principalmente con los laterales de las plantillas de transporte de piezas. No se simularon todas las colisiones debido al alto coste computacional y los errores que se pueden presentar en la simulación en caso de hacerlo, dando a lugar a situaciones que no reflejan apropiadamente el comportamiento de un sistema físico real.
Dentro de NX se crearon señales virtuales conectadas a los sensores y actuadores, de tal forma que se simulara apropiadamente el método de control de los actuadores y la lectura de los sensores por parte del PLC, garantizando por ejemplo que un sensor normalmente abierto o normalmente cerrado, expusiera una señal que emulara dicho comportamiento, y por lo tanto no requiera una modificación al código Ladder ejecutado por el PLC, en caso de controlar un sistema físico real.

La implementación completa se encuentra en la sección [Industria 4.0](https://apm-kullu.github.io/kulluWebSite/industria/) 


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
        onclick="window.location.href = window.location.origin + '/kulluWebSite/scada'">
Ver SCADA </button>