---
layout: page
title: Industria 4.0
---
Para nuestra solución, se creó  un servidor de Ignition en la nube de a través de Amazon Web Services. Se generó una imagen  de este servidor (Amazon Machine Image) y se lanzó una instancia en Elastic Cloud Computing (EC2) para activar el servidor. En este se instalaron tres extensiones  de MQTT: Distributor, Engine y Transmission, luego  se instalaron servidores de Ignition en  tres partes diferentes. El primero a la  izquierda es una versión compacta llamada Ignition Edge (instalada debido a temas de recursos limitados en la PC),este servidor cuenta con dos módulos de  MQTT Transmission que envía los datos de  los dispositivos conectados a la nube, y MQTT Engine que recupera los datos de la nube. Los servidores de en medio y la derecha  son Gateways al igual que el de la nube y también cuentan con los módulos MQTT Transmission y Engine, estos módulos  permiten el intercambio de información  entre los servidores de Ignition que están fuera de la nube. El servidor en el centro se comunica a  través de OPC con Kepware, lo que permite  el intercambio de información con el robot y el servidor de la derecha también se comunica mediante OPC con RSLinx, lo que permite la  conexión con el PLC y Siemens NX.

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
