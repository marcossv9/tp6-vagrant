## Configurar VM Ubuntu

Vagrant.configure("2") do |config| #apertura archivo Vagrant
  config.vm.define "ubuntu" do |ubuntu| #definición VM para Ubuntu
    ubuntu.vm.hostname = "ubuntuvm" #hostname VM
    ubuntu.vm.box = "ubuntu/xenial64" #box de vagrantcloud a utilizar
    ubuntu.vm.network "forwarded_port", guest: 3306, host: 53306 #exponiendo puerto 3306 de la VM
    ubuntu.vm.provision "shell", inline: <<-SHELL #aprovisionamiento por shell
      sudo add-apt-repository ppa:deadsnakes/ppa #agrego repo de python3.6
      sudo apt-get update -y
      sudo apt-get install python3.6 -y #instalación python
      debconf-set-selections <<< 'mysql-server mysql-server/root_password password root' #configuración de password usuario de la BD root/root
      debconf-set-selections <<< 'mysql-server mysql-server/root_password_again password root'
      sudo apt-get install mysql-server -y  #instalación MySQL
      curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash - #instalación NodeJS
      sudo apt-get install -y nodejs
      echo "INSTALACIÓN COMPLETA"
      SHELL
  end
end