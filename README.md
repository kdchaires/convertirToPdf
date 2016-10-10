# convertirToPdf
Vagrant que contiene una aplicación en php para convertir archivos con extensión .txt .doc .docx .xls .xlsx a pdf.

##1.  Necesitamos instalar vagrant.
<https://www.vagrantup.com>	

##2.  Instalar virtualbox.
<https://www.virtualbox.org>

##3.  En la ruta que desees, crea una carpeta para los archivos de vagrant.

    $mkdir ~/Documentos/centos_txtTopdf
##4.  Desde linea de comandos, accede a la carpeta que creaste.

##5. Descargar e instalar el box, esto lo podemos hacer de dos maneras:  

	1.- Ejecutando el siguiente comando:
    
    $vagrant init kchaires/centos_txtTopdf; vagrant up --provider virtualbox
    
2.- b) Descargar el vagrant e iniciar el vagrant:
Descargar el archivo box desde: <https://atlas.hashicorp.com/kchaires/boxes/centos_txtTopdf/versions/1.0.0/providers/virtualbox.box>


Renombrar el archivo a centos_txtTopdf.box

    $mv hc-download.crdownload centos_txtTopdf.box

Agrega centos.box a la lista de vagrant

    $vagrant box add centos_txtTopdf centos_txtTopdf.box

Iniciar el vagrant

    $vagrant init centos

Esto genera un archivo vagrant (archivo de configuración) y una carpeta .vagrant (contiene archivos necesarios para la virtual).

##6.  Automáticamente se crearán algunos archivos, modifica el archivo Vagrantfile agregando la siguiente línea en la sección “Create a forwared port mapping...”

config.vm.network
 "forwarded_port", guest: 80, host: 3000

##7.  Re-iniciar el Vagrant.
    $vagrant reload

##8.  Listo, con esto ya podrás tener acceso al módulo para poder convertir tus archivos, abre un explorador y teclea la siguiente dirección.

<http://localhost:3000/convertir>
