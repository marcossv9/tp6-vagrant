# tp6-vagrant

Creación de una VM con Vagrant sobre Ubuntu que contenga Python 3.6, mysql y NodeJS 10.15.0 preinstalado.

## Puesta en marcha rápida

- Para poner en marcha el proyecto de forma rápida con Vagrant, ejecutar lols siguientes comandos:


```
git clone https://github.com/marcossv9/tp6-vagrant.git
vagrant up
```

- Para poner en marcha el proyecto usando imagen base de Ubuntu con Vagrant y Ansible playbook, realizar lo siguiente:

```
git clone git clone https://github.com/marcossv9/tp6-vagrant.git
cd ansible
vagrant up
```

## Empezando

Estas instrucciones te llevarán a obtener una copia de este proyecto arriba y corriendo en tu máquina local para propósitos de desarrollo o testeo. Ve las notas de insalación para replicar el entorno en tu sistema.

### Prerequisitos

Se necesita tener instalado lo siguiente para SO Ubuntu:

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

### Instalación

Paso a paso de las instalaciones necesarias para correr Vagrant.

- Instalar Vagrant y VirtualBox

```
sudo apt-get install vagrant
sudo apt-get install virtualbox
```

Se pueden obtener las distintas boxes base desde [VagrantCloud](https://vagrantcloud.com/). Para este caso usaremos la de ubuntu/xenial64.

### Preparación

- Crear un directorio para nuestro proyecto y generar el archivo [Vagrantfile](https://github.com/marcossv9/tp6-vagrant/Vagranfile)

```
cd /
mkdir proyecto
touch Vagrantfile
```

- Escribir dentro del archivo Vagrantfile con algn editor de texto, el contenido de [éste](https://github.com/marcossv9/tp6-vagrant/blob/master/Vagrantfile) archivo.

- Inicializar el archivo Vagrantfile:

```
vagrant init
```

### Ejecución

- Inicializar VM

```
vagrant up
```

## Autor

* **Marcos Silva** - *Computer Systems Engineer* - [marcossv9](https://github.com/marcossv9)