## Configurar VM Ubuntu

Vagrant.configure("2") do |config| #Apertura archivo Vagrant
  configure.vm.define "ubuntu" do |ubuntu| #Definición VM para Ubuntu
    ubuntu.vm.hostname = "ubuntu" #hostname VM
    ubuntu.vm.box = "ubuntu/xenial64"
    ubuntu.vm.network = "private_network", ip: "172.16.0.10"
    ubuntu.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update -y
      sudo apt-get install python3.6 -y
    SHELL
  end
end