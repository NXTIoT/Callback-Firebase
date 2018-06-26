# Callback-Firebase
Repositorio donde se muestra la creación de un callback a Firebase

Ejemplo de temperatura
------
antes de comenzar a enviar datos a Firebase primeramente realizaremos el ejemplo de temperatura en nuestro devkit

[-Ejemplo de temperatura](https://github.com/NXTIoT/NXTIoT_DEVKIT#sensor-de-temperatura)

Google Firebase
--------------
En esta sección realizaremos un Callback hacia Firebase la API de Google utilizando el ejemplo del sensor de temperatura y se enviara la información al Realtime Database. Lo que necesitamos es:
<br />-Una cuenta de Google
<br />-crear un nuevo proyecto en firebase

Entramos a la consola de Firebase con nuestra cuenta de Google y creamos un nuevo proyecto haciendo click en añadir proyecto

![firebase](https://raw.githubusercontent.com/amastache/Firebase-callback/5026dc13165e757e931f5d9798cd388e4d22279a/consol.png)

Le damos un nombre a nuestro proyecto, seleccionamos el país de donde nos encontramos y aceptamos las condiciones para que nos permita crear un nuevo proyecto

![firebase](https://raw.githubusercontent.com/NXTIoT/Callback-Firebase/master/imagen/f2.png)

Una vez creado el proyecto hacemos click en Desarrollo/Database y en la sección Realtime Database damos click en Empezar

![firebase](https://raw.githubusercontent.com/NXTIoT/Callback-Firebase/master/imagen/f3.png)

Seleccionamos Empezar con el modo de prueba para que nos permita escribir sobre el Realtime Database sin ningún problema, estas reglas pueden modificarse posteriormente, hacemos click en Habilitar


![firebase](https://raw.githubusercontent.com/NXTIoT/Callback-Firebase/master/imagen/f4.png)

Una vez creada el Realtime Database copiamos la url con el formato https:// [PROJECT_ID]. firebaseio.com/ que aparece en la parte superior

![firebase](https://raw.githubusercontent.com/NXTIoT/Callback-Firebase/master/imagen/f5.png)

Configuración del Callback
----------
Regresamos al backend de sigfox para crear el Callback. Nos vamos a nuestro dispositivo y damos click en el "Device Type"

![firebase](https://raw.githubusercontent.com/NXTIoT/NXTIoT_DEVKIT/master/images/azure8.png)

Dentro de la sección 'Callbacks' damos click en 'New', seguido daremos click en 'Custom Callback'

![firebase](https://raw.githubusercontent.com/Iotnet/IoTnet_DEVKIT/master/images/callback.png)

En la ventana que nos aparece pegamos la url que copiamos de la consola de firebase en la sección Url pattern y configuraremos nuestro callback de la siguiente manera:

![firebase](https://raw.githubusercontent.com/NXTIoT/Callback-Firebase/master/imagen/f6.png)

Damos Click en "Ok" y con eso queda creado nuestro Callback. Ahora verificaremos que no exista ningun error. Damos click en "Associated devices" y hacemos click en el ID de nuestro Devkit

![firebase](https://raw.githubusercontent.com/NXTIoT/Callback-Firebase/master/imagen/f7.png)

y en el panel izquierdo nos vamos a "Messages" para visualizar el estatus del Callback. Presionamos el boton de nuestro Devkit para mandar un mensaje. Si todo fue correctamente configurado la flecha en Callbacks ahora permanecerá en verde como se muestra en la imagen

![firebase](https://raw.githubusercontent.com/NXTIoT/Callback-Firebase/master/imagen/f8.png)

Regresamos al Realtime Database y ya obtenemos el dato recibido por el backend

![firebase](https://raw.githubusercontent.com/NXTIoT/Callback-Firebase/master/imagen/f9.png)


