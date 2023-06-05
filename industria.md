---
layout: page
title: Industria 4.0
---

Para nuestra solución, se creó  un servidor de ignation en la nube de Amazon web Services, Se generó una imagen  de este servidor en Amazon Machine image  y se lanzó una instancia en elastic  Cloud computing para activar el servidor  en la nube de Amazon, en el servidor de  la nube se instalaron tres extensiones  de mqtt  distributor engine y Transmission, luego  se instalaron servidores de ignición en  tres partes diferentes, el primero a la  izquierda es una versión compacta  llamada ignition nets,  este servidor cuenta con dos módulos de  mqtt transmisión que envía los datos de  los dispositivos conectados a la nube y  engine que recupera los datos de la nube. Los servidores de en medio y la derecha  son gateways al igual que el de la nube  y también cuentan con los módulos mqtt  transmisión y engine, estos módulos  permiten el intercambio de información  entre los servidores de ignition que  están fuera de la nube,  el servidor en el centro se comunica a  través de opc con kepware, lo que permite  el intercambio de información con el  robot a través de robot y el servidor de  la derecha también se comunica mediante  opc con Ares links, lo que permite la  conexión con el plc y siemens MX 

![image](https://github.com/APM-Kullu/Project/assets/52173621/8f3521af-854a-45ab-8b39-e819512413d9)

Video de la implementación

[![Alt text](https://img.youtube.com/vi/rG_0yiJnTqWK_8.jpg)](https://www.youtube.com/watch?v=0yiJnTqWK_8)

Video de la Implementación de Ignition Gateway en AWS

[![Alt text](https://img.youtube.com/vi/nD5rSWWMgQA.jpg)](https://www.youtube.com/watch?v=nD5rSWWMgQA)

Los tableros de Control son los siguientes

<img width="513" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/6b0092cb-2f16-4e01-b9c4-732336aeac69">

<img width="517" alt="image" src="https://github.com/APM-Kullu/Project/assets/52173621/c4b7b7b2-91ce-439c-95f8-e5f1e99d9c3c">


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