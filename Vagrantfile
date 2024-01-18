# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/jammy64"
  config.vm.network "private_network", ip:"192.168.169.50"
  config.vm.synced_folder "src", "/home/vagrant/html"
  config.vm.provision "file", source:"docker-compose.yml", destination:"$HOME/"
  config.vm.hostname="itopHost"
  config.vm.provider "virtualbox" do |v|
       v.memory = 2048
	   v.cpus= 2
	   v.name="Itsm_server"
	end
   config.vm.provision "shell", path:"install-docker.sh"
end
