# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "hashicorp/precise32"
  config.vm.network "private_network", ip: "192.168.50.4"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end

  config.vm.provision "shell", inline: <<-SHELL
     sudo apt-get update
     sudo apt-get -y install python-dev
     sudo apt-get -y install vim
     sudo apt-get -y install python-pip
     sudo apt-get -y install python-sklearn
     sudo apt-get -y install git
     sudo pip install nltk
     sudo python -m nltk.downloader -d /usr/share/nltk_data all
  SHELL
end
