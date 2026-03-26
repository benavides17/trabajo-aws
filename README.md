# trabajo-aws
Actividad Evaluativa 2

 

Estudiante: 
Ronald Felipe Benavides Bastidas
Id: 
507967



Docente:  

Duarte Eraso


Asignatura: Electiva II


Universidad Cooperativa de Colombia
Facultad de Ingeniería



Objetivo General

Diseñar e implementar una solución serverless que permita a los usuarios subir imágenes desde una interfaz web, procesarlas automáticamente mediante eventos y descargarlas una vez transformadas.

Objetivos Específicos
Implementar un sistema de almacenamiento en la nube para imágenes.
Configurar eventos automáticos para el procesamiento de archivos.
Desarrollar una función que modifique las imágenes.
Crear una interfaz web para interacción con el usuario.
Garantizar el acceso controlado a los recursos.

Descripción General Del Sistema
El sistema desarrollado funciona de la siguiente manera:
El usuario accede a una página web.
Selecciona una imagen desde su dispositivo.
La imagen se carga en un almacenamiento en la nube.
Se activa automáticamente un proceso de transformación.
Se genera una nueva imagen procesada.
El usuario puede visualizar y descargar el resultado.


Desarrollo Del Proyecto (Paso A Paso)

reacción del almacenamiento (S3)
Se creó un contenedor de almacenamiento donde se guardan las imágenes.
Configuraciones realizadas:
Se definió un nombre único para el bucket.
Se seleccionó la región correspondiente.
Se deshabilitó el bloqueo de acceso público para permitir interacción desde el navegador.
Se configuró CORS para permitir solicitudes externas.
 

Configuración del hosting web
Se subió el archivo index.html al almacenamiento.
Se habilitó:
Hosting de sitio web estático.
Acceso público al archivo.
Esto permitió acceder a la interfaz desde el navegado
 
Creación de la función de procesamiento
Se creó una función que se ejecuta automáticamente cuando se sube una imagen.
Configuraciones:
Nombre de la función.
Lenguaje de programación.
Permisos básicos para ejecución.

implementación del código de procesamiento
La función desarrollada realiza las siguientes acciones:
Obtiene la imagen cargada.
Guarda una nueva versión de la imagen.
Se agregó una validación importante para evitar que la función procese imágenes ya transformada
 

Instalación de dependencias
Para procesar imágenes se utilizó una librería especializada.
Pasos realizados:
Crear carpeta de trabajo.
Inicializar proyecto.
Instalar dependencia.
Crear archivo principal.
Comprimir archivos.
Subir a la función.

Solución de errores durante el desarrollo

Durante la implementación se presentaron varios problemas:

Error de permisos (AccessDenied)
Problemas de configuración CORS
Errores en credenciales
Problemas de descarga de imágenes

Estos se solucionaron ajustando:

Políticas de acceso
Configuración de seguridad
Código del frontend

Conclusiones

La implementación de esta arquitectura serverless con AWS S3, Lambda e IAM demostró que es posible construir aplicaciones funcionales, seguras y escalables sin necesidad de gestionar infraestructura tradicional. La integración entre los tres servicios permitió automatizar el flujo completo de carga, procesamiento y almacenamiento de imágenes de forma eficiente y con mínima intervención manual.
Entre los principales beneficios observados destacan la reducción de costos operativos gracias al modelo de pago por uso, la escalabilidad automática ante variaciones en la demanda, y la simplificación del mantenimiento al eliminar la gestión de servidores. Además, el uso de políticas IAM bajo el principio de mínimo privilegio garantizó un control de acceso seguro en cada componente del sistema.
En conjunto, este proyecto confirma que el enfoque serverless representa una alternativa sólida y moderna para el desarrollo en la nube, con una base fácilmente extensible hacia servicios adicionales como API Gateway, CloudFront o Step Functions según las necesidades futuras del sistema.

