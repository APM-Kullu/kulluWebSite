---
layout: page
title: KPIs
---

# Parámetros de rendimiento  y KPIs

De acuerdo con el [diagrama VSM](https://drive.google.com/file/d/1R6CTQlbLSqZXP_ZOIvwtcjmw3XsWAsQU/view?usp=share_link) diseñado para nuestro proyecto, se cuenta con una línea de producción compuesta por 6 etapas:
1. Corte láser
2. **Taladrado:** Presenta una bifurcación para el procesamiento independiente de piezas planas y piezas que requieren una orientación específica.
3. Lijado
4. Sellado
5. Lacado
6. **Ensamble:** Presenta una ramificación de 3 líneas, para el ensamblaje independiente de los 3 productos que se trabajarán.
<br><br>

### Trabajo en proceso (WIP):
Para cada producto el proceso de manufactura será secuencial y abarcará cada una de las 6 etapas descritas. Esto implica la existencia de 5 almacenes intermedios y 6 estaciones, por producto. Por tanto, la expresión para estimar el WIP está dada por:

![image](https://user-images.githubusercontent.com/52173621/227734057-33b0f70c-aad0-4f3a-9607-26930d2fe5dc.png)

### Takt time:

### Tiempo de ciclo ($T_c$):


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
        onclick="window.location.href = window.location.origin + '/kulluWebSite/economica'">
Ver Evaluación económica </button>