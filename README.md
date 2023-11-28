# OxxoConcentracionIA
Este repositorio contiene la información necesario para poder ejecutar la prueba de concepto propuesta como solución a la problemática otorgada para la Concentración de Inteligencia Artificial Avanzada para la Ciencia de Datos II.

Barredez Rios, Carlos Andres - A01653183
Delgado Rios, Leonardo - A00827915
Joseph Hure, Marin - A01762723
Sánchez Pérez, Raúl Andrés - A01367635

## Carpeta de Drive que contiene los pesos del modelo final de YOLO:

Link Repositorio de Drive -> https://drive.google.com/drive/folders/1k2Y1uVm_c2jd1B6xilwNXmmXYgmidZ8b

## Link al video de ejecución de nuestra solución:

Link Video de Ejecución de la Prueba de Concepto -> https://www.youtube.com/watch?v=YUy2diA3xOk

## Instalación local para la ejecución del código:

> (Ambiente de desarrollo utilizado fue **VSCode.**)

> De igual manera, se asume que se tiene descargado Python en su versión 3.10.7 y la librería pip.

Realizar la instalación y activación de Rabbit MQ -> https://www.rabbitmq.com/install-windows.html#downloads

De igual manera, será necesario realizar la instalación de las siguientes librerías a través de una linea de comandos, las cuales nos ayudarán a ejecutar de manera local/temporal (debido a las limitaciones de nuestro tenant en Oracle Cloud Infrastructure) :

> python -m pip install Django

> pip install celery

> pip install eventlet

> pip install oracledb

> pip install ultralytics==8.0.196

> pip install Pillow

Al descargar el código, estarán organizados de la siguiente manera:

>   proj/

>     proj/

>     app1/

>     yoloWeights/ *** (Descargar pesos de la carpeta de Drive e ingresar los archivos .pt dentro de esta carpeta)

>     manage.py

Una vez realizada la instalación de las librerías y la descarga de los pesos, ubicandonos en la carpeta raíz abrir dos diferentes lineas de comados.
Ejecutar el siguiente comando en la primera :

> celery -A proj worker -l info -P eventlet

Ejecutar el siguiente comando en la segunda, para habilitar la comunicación entre servidores de manera paralela : 

> celery -A proj beat -l info

Portal de la aplicación "Administración" -> https://g0c4542b6212cd4-dboxxomlapp.adb.us-phoenix-1.oraclecloudapps.com/ords/r/oxxo_testing/administraci%C3%B3n

Portal de la aplicación "Oxxo RackWise" -> https://g0c4542b6212cd4-dboxxomlapp.adb.us-phoenix-1.oraclecloudapps.com/ords/r/oxxo_testing/oxxo-rackwise

*** IMPORTANTE: No se tendrá acceso a los portales a menos que se establezca la autorización en Oracle Cloud Infrastructure.
