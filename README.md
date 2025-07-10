# Capstone-Colombo-Homero-TUP-ARQ
El informe técnico se encuentra en la carpeta "Documentacion"

Explicación de proyecto Capstone: "Visualización de datos IoT en entorno contenerizado con Node-RED y Docker"

Este proyecto consiste en el desarrollo de una solución funcional y contenerizada que permite consultar datos en tiempo real desde un dispositivo IoT simulado mediante una API REST, procesarlos y visualizarlos de manera clara utilizando Node-RED, una herramienta de programación visual.

Toda la solución se ejecuta dentro de un contenedor Docker, lo que garantiza portabilidad, aislamiento y facilidad de despliegue. La arquitectura se define mediante un archivo docker-compose.yml que permite levantar automáticamente el entorno con un solo comando.

 Componentes principales:
Node-RED: herramienta de flujo visual para integrar, transformar y visualizar datos.

Docker + Docker Compose: para contenerizar y orquestar el servicio de Node-RED.

API pública: simula un dispositivo IoT que entrega datos como temperatura, humedad y presión.

Dashboard Web: interfaz donde se visualizan los datos en tiempo real mediante widgets.

 Funcionamiento general:
Un nodo inject se ejecuta automáticamente cada 40 segundos.

Ese nodo activa una consulta HTTP (http request) a la API del dispositivo.

El resultado (JSON) se convierte en un objeto utilizable.

Dos nodos function ordenan y filtran los dos datos más recientes.

Esos datos se visualizan en tiempo real con widgets tipo gauge y plantillas personalizadas en un dashboard accesible vía web.

Objetivo alcanzado:
El objetivo fue demostrar la capacidad de desplegar una solución funcional IoT en un entorno contenerizado, utilizando herramientas modernas de desarrollo y administración de servicios. El proyecto cumple con los principios de automatización, modularidad y reutilización que exige la arquitectura de sistemas operativos contemporáneos.

El docker-compose se corre entrando a la carpeta en la que esta ubicado el archivo docker-compose.yml y ejecutando el comando docker compose up -d
 
docker compose → ejecuta el comando usando Docker Compose (plugin moderno)

up → "levantar" los servicios definidos

-d → modo "detached", o sea, en segundo plano (no queda la terminal ocupada)

 Si todo está bien configurado, el contenedor de Node-RED se va a levantar y quedar corriendo en segundo plano.


Enlace video: https://drive.google.com/drive/folders/1IOdFb-PJhuMlX_ZqHnfSisr810VzTluV?usp=drive_link

Autor: Homero Colombo (23086)
