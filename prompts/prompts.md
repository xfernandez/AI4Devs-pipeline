## Presentación del proyecto

´´´
Actua como ingeniero de software senior, especializado en desplegar en AWS usando github actions. Tienes un perfil devops y por eso te han pasado un ultimo proyecto que debes liderar su despliegue. Te vas a centrar en el @backend del proyecto ya que es lo qu debemos desplegar en una maquina de Ec2 en git actions. Es por ello que te voy a pedir prinmero que crees una carpeta documentacion dentro de la carpeta backend donde pondremos un fichero analisis_backend.md en donde detallaras toda la información que debo conocer para dominar el proyecto. Mira las tecnologias que usa mirando el @package.json, analiza como esta organizado el codigo y como este backend puede ser desplegado. Es importante que hagas este analisis para que luego te sea mas facil generar la automatizacion. Tomate el tiempo que creas necesario y hazme preguntas si crees que va mejorar la calidad de tu trabajo. Se meticuloso y crítico con tu resultado.
´´´

´´´
creo que para la base de datos, el @docker-compose.yml sugiere que es un postgreSQL. El dominio para ahora no es importante. No tengo la instancia. Podemos crearla luego dinamicamente desde el CD/CI no? No pensemos en monitorizacion por ahora. Y a nivel de seguridad sigue los standard pero hazlo sencillo. Estamos en una practica.
´´´

´´´
por el momento, como en local puedo ver como se arranca el backend y pasa todos los tests que tiene? Primero recuerdame como arranco el docker para tener la db
´´´

## Creacion del workflow

´´´
Vale, ahora vamos a realizar un github action. Este debe hacer lo siguiente:
- Primero de todo el workflow se va poder ejecutar automaticamente cuando entramos a master una PR o manualmente si el usuario lo desea.
- Segundo vamos a pasar los tests existentes en el backend
- Tercero generaremos un build del backend
- Crearemos una maquina virtual de forma dinamica en EC2
- Nos conectaremos a ella y desplegaremos el backend en ella. en este ec2 se tiene que instalar un docker, para poder ejecutar el @docker-compose.yml y arrancar el container en la base de datos. Vamos a tener que volver a generar los datos en prisma en la db que esta en el docker que hemos instalado en ec2 y finalmente arrancaremos.
Tomate el tiempo que sea neceario para hacer un trabajo excelente. Usa las buenas practica de github actions y dame el detalle de la configuracion de keys y variables que debo hacer en mi proyecto.
´´´

´´´
Vamos a mejorar un detalle. Soy muy sensible al coste, puedes hacer que la vm que se cree sea de tipo SPOT? Estamos en pruebas, creo que es lo mejor para optimizar el coste. Tomate el tiempo que necesites
´´´

´´´
Guiame paso a paso para obtener las siguientes variables:
EC2_SECURITY_GROUP_ID
EC2_SUBNET_ID
EC2_SSH_KEY
´´´

´´´
Ok, en el entorno que estoy no tengo instalado la libreria de AWS, no me acuerdo como se hacia. Puedes ayudarme a configurarmela e ir paso a paso recuperando la informacion que necesito
´´´

### A partir de aquí ya han sido prompts para arreglar errores hasta el deploy final
