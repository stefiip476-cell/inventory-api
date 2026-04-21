API de Inventario Tecnológico
Descripción

Este proyecto consiste en el desarrollo de una API utilizando FastAPI, enfocada en la gestión de dispositivos tecnológicos. Su objetivo principal es permitir el control de un inventario de equipos como laptops, routers y otros dispositivos, facilitando el manejo de su información de forma sencilla.

La API permite interactuar con los datos mediante diferentes endpoints, simulando el funcionamiento básico de un sistema de inventario.

Funcionalidad

La API cuenta con varias funcionalidades que permiten gestionar completamente los dispositivos. En primer lugar, es posible registrar nuevos equipos mediante el endpoint POST /devices, donde se envía la información del dispositivo como su nombre, tipo, marca y estado.
<img width="1240" height="572" alt="image" src="https://github.com/user-attachments/assets/b19f3eea-1b32-4348-942e-19d3f2fc04d6" />


Una vez registrados, los dispositivos pueden ser consultados utilizando GET /devices, lo que devuelve el listado completo del inventario.
<img width="1250" height="572" alt="image" src="https://github.com/user-attachments/assets/3190fa63-55c7-42c3-bd4b-077805f6bfe5" />


También se implementó la posibilidad de actualizar el estado de un dispositivo mediante PUT /devices/{id}, lo cual permite modificar su condición, por ejemplo, de activo a dañado o en mantenimiento.

En caso de que un dispositivo ya no sea necesario, puede eliminarse del sistema utilizando DELETE /devices/{id}, removiéndolo completamente del inventario.
<img width="1252" height="625" alt="image" src="https://github.com/user-attachments/assets/aab0a2a1-1e79-4095-bbfb-8690b6432a61" />


Como funcionalidad adicional, la API incluye el endpoint GET /devices/count, el cual permite obtener un conteo de los dispositivos agrupados por tipo. Esto resulta útil para tener una visión general del inventario.

Finalmente, se cuenta con un endpoint básico GET / que permite verificar que la API se encuentra en funcionamiento.

Tecnologías utilizadas

El desarrollo fue realizado utilizando Python junto con FastAPI, un framework moderno para la creación de APIs. Para ejecutar el servidor se utilizó Uvicorn.

Ejecución del proyecto

Para ejecutar la API, primero se deben instalar las dependencias necesarias:

pip install -r requirements.txt

Luego, se inicia el servidor con el siguiente comando:

uvicorn main --reload

Una vez en ejecución, la API puede ser probada desde el navegador accediendo a:

http://127.0.0.1:8000/docs
