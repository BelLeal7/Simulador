# TPI Organización Empresarial - Bot de Gestión de Turnos

Este repositorio contiene la simulación del código para el Trabajo Práctico Integrador de la materia Organización Empresarial. 

El proyecto consiste en un chatbot diseñado para automatizar el proceso administrativo de **Gestión de Turnos** de un centro de estética. El objetivo es permitir que los clientes realicen sus reservas de manera rápida y estructurada, validando la lógica del diagrama de negocio (BPMN 2.0).

## 🚀 Características Técnicas Implementadas

Para cumplir con los requerimientos de la cátedra, el simulador incluye:

1. **Máquina de Estados Finito (FSM):** El bot tiene "memoria" y rastrea el progreso del usuario a través de los estados: `ESPERANDO_SALUDO`, `SELECCIONANDO_SERVICIO`, `SELECCIONANDO_PROFESIONAL`, `ELIGIENDO_FECHA_HORA` y `CONFIRMANDO_TURNO`.
2. **Manejo del "Camino Infeliz":** El sistema es robusto ante errores de entrada. Si se espera un número y el usuario ingresa texto, el bot intercepta el error, informa al usuario y se mantiene en el mismo estado solicitando el dato correcto.
3. **Persistencia de Datos Simulada:** Cuenta con un diccionario de datos en memoria para verificar la existencia de los profesionales (identificados con la variable `nro`) y para almacenar el registro final de cada turno confirmado.

## 🛠️ Tecnologías

* **Entorno de ejecución:** Node.js
* **Interfaz:** Consola (Línea de comandos)

## ⚙️ Instrucciones de Instalación y Uso

Para ejecutar esta simulación en tu entorno local, sigue estos pasos:

1. Asegúrate de tener [Node.js](https://nodejs.org/) instalado en tu computadora.
2. Clona este repositorio o descarga el archivo `simulador.js`.
3. Abre una terminal (consola) y navega hasta la carpeta donde se encuentra el archivo.
4. Ejecuta el siguiente comando para iniciar el bot:

   ```bash
   node simulador.js
5. Interactúa con el bot escribiendo mensajes en la consola. Puedes enviar un "Hola" para comenzar el flujo o intentar ingresar datos incorrectos para probar el camino infeliz.
