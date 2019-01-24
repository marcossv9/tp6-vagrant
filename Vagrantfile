## Configurar VM Ubuntu

Vagrant.configure("2") do |config| #Apertura archivo Vagrant
  config.vm.define "ubuntu" do |ubuntu| #Definición VM para Ubuntu
    ubuntu.vm.hostname = "ubuntuvm" #hostname VM
    ubuntu.vm.box = "ubuntu/xenial64"
    ubuntu.vm.network "private_network", ip: "172.16.0.10"
    ubuntu.vm.provision "shell", inline: <<-SHELL
      sudo add-apt-repository ppa:deadsnakes/ppa
      sudo apt update -y
      sudo apt install python3.6 -y
      SHELL
  end
end