# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Define SO e hostname
  config.vm.box = "eunati/debian-jessie64-puppet5"
  config.vm.host_name = "desafiosensedia"
  
  config.vm.network "forwarded_port", guest: 5000, host: 5000, host_ip: "127.0.0.1"
  
  config.vm.provision "puppet"
  
config.vm.provision "shell", inline: <<-SHELL
	sudo apt-get update
	sudo apt-get install unzip -y
	sudo mkdir /sensedia
	sudo wget https://depositfiles.s3.amazonaws.com/candidato/app-candidato.zip -O /sensedia/app-candidato.zip
	sudo unzip /sensedia/app-candidato.zip -d /sensedia/
	sudo docker build -t app-candidato /sensedia/app-candidato/.
	sudo docker run -p 5000:5000 -e CODIGO_CANDIDATO=yze0ymrlmmy0 app-candidato &
  SHELL
  
end
