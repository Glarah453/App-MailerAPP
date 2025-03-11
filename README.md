Proyecto MAilerAPP
==================

Creación de una Aplicación Web para enviar correos con [Python 3.9.6](https://www.python.org/downloads/release/python-396/), el microframework [Flask](https://flask.palletsprojects.com/en/2.0.x/) que permite crear Aplicaciones Web bajo el patrón [MVC](https://developer.mozilla.org/es/docs/Glossary/MVC), [HTML](https://desarrolloweb.com/home/html) + [CSS3](https://openwebinars.net/blog/que-es-css3/) para la estructura de y diseño de la Aplicación, [MySql](https://www.mysql.com/) un sistema de administración de base de datos relacionales, [SendGrid](https://sendgrid.com/) basado en una nube para envía emails transaccionales y de marketing a cientos de miles de clientes, [Heroku](https://dashboard.heroku.com/apps) que es una plataforma en la nube que permite a las empresas construir, entregar, supervisar aplicaciones y alojarlas en la nube con un plan gratis LIMITADO.

Informacion General
-------------------

Este Proyecto tiene como fin poder enviar correos desde una App a un correo personal verificado por [SendGrid](https://pypi.org/project/sendgrid/) que nos permite enviar más de 100 correos gratis por el dia. Este proyecto pone en practica la programación de la recepcion de correos de una empresa con Python 3.9 y el microframework Flask y una base de datos de MySql Workbench. Para la estructura de la aplicación Web se uso HTML5 con los bloques de Django que es un framework de desarrollo web de código abierto, escrito en Python, que respeta el patrón de diseño conocido como modelo–vista–controlador (MVC), y para el diseño de la interfaz de la aplicación se uso CSS3.

Para este proyecto utilizamos [Git](https://git-scm.com/downloads) + [Github](https://github.com/join)
más los siguientes librerias de Python3.

Instalación
------------
* Instalar [Python 3.9](https://www.python.org/downloads/release/python-396/) e instalar estas librerias con [pip](https://pypi.org/project/pip/):
  - [FLASK](https://flask.palletsprojects.com/en/2.0.x/) para el servidor.
  - [SendGrid](https://pypi.org/project/sendgrid/) para enviar correos desde la APP a uno personal.
  - [Python-DotEnv](https://pypi.org/project/python-dotenv/) para las variables de entorno que ocupara la APP.
  - [MySql-Connector-Python](https://pypi.org/project/mysql-connector-python/) para la conexión y consultas de la base de datos.
  - [Gunicorn](https://pypi.org/project/gunicorn/) para servir todo lo dinámico de un proyecto en un servidor.

* Instalar [MySql Workbench 8.0](https://www.mysql.com/products/workbench/) con servidor y crear una conexion localhost con el puerto y los permisos del usuario requeridos para ingresar desde el servidor Flask desde la APP.

* Crear una cuenta en [SendGrid](https://sendgrid.com/) siguiendo todos sus pasos, luego crear una API key que sera una variable de entorno para asi al tener verificado un DOMINIO (si no haces esto, no recibiras los correos enviados desde la APP) con nuestro correo que usaremos como Bandeja de Entrada de todos los correos que enviemos dentro de la APP.

* Crear una cuenta en [Heroku](https://dashboard.heroku.com/apps) siguiendo todos sus pasos, luego ingresar una tarjeta de credito para poder ocupar una base de datos gratis que nos da Heroku llamada [Ignite](https://elements.heroku.com/addons/cgignite), es necesario ingresar una tarjeta para obtener los privilegios que da Heroku o no se podra subir la APP con una base de datos y no funcionara del todo (al ingresar la tarjeta y subir la APP, no se hacen CARGOS en la TARJETA).

* Subir la APP a [Git](https://github.com/join) con la rama 'MAIN', crear el archivo .gitignore para subir solo lo necesaerio, hacer un commit de inicialización, crear la APP con 'heroku create', creamos la base de datos con 'heroku addons:create cleardb:ignite', configuramos las variables de entorno en Heroku con la direccion de nuestra APP que nos creo anteriormente, crear el archivo requirements.txt con 'pip freeze > pip freeze > requirements.txt, crear el arhivo Procfile con el comando 'echo "web: gunicorn app:'create_app()'" > Procfile', configurar la variable 'SendGrid_Key' con el comando 'heroku config:set SENDGRID_KEY=***clave generada en sendgrid*****', Ahora subimos los archivos nuevos al repositorio, hacemos un commit para los archivos nuevos, y subimos el repositorio a la nube de Heroku con 'git push heroku main', y abrimos la APP con 'heroku open'.


Resultado del Proyecto
======================

https://glacial-retreat-11080.herokuapp.com/

NOTA: si tu proyecto funcionó no pases la APP para envios masivos de correos, SendGrid permite enviar 100 correos gratis durante el dia, y si ocupaste un correo de una empresa global como Google, Outlook, etc. evita enviar muchos correos para que asi la empresa no los tome todos como spam.



