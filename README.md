# convertirToPdf
Vagrant que contienen una aplicación en php para convertir archivos con extensión .txt .doc .docx .xls .xlsx a pdf.

##1.  Necesitamos descargar Vagrant.
	https://www.vagrantup.com/downloads.html	

##2.  Instalar Vagrant.
	https://www.vagrantup.com/docs/installation/

##3.  En la ruta que desees, crea una carpeta para los archivos de vagrant.

    $ mkdir ~/Documentos/centos_txtTopdf
##4.  Desde linea de comando, accede a la carpeta que creaste.

##5.  Ejecuta el siguiente comando:
    $ vagrant init kchaires/centos_txtTopdf; vagrant up --provider virtualbox

Esto creara un archivo Vagrant (archivo de configuración) y una carpeta .vagrant (contiene archivos necesarios para la virtual).

##6.  Automáticamente se crearán algunos archivos, modifica el archivo Vagrantfile agregando la siguiente línea en la sección “Create a forwared port mapping...”

config.vm.network
 "forwarded_port", guest: 80, host: 3000

##7.  Re-iniciar el Vagrant.
    $ vagrant reload

##8.  Listo, con esto ya podrás tener acceso a modulo para poder convertir tus archivos, abre un explorador y teclea la siguiente dirección.

	http://localhost:3000/convertir
