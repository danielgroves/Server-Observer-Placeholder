# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # Envronment Name
  config.vm.box = "precise64"

  # Where to find environment for first time
  #config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  # Map a port from host to vagrant machine
  # config.vm.network :forwarded_port, guest: 80, host: 8080

  # Host-only IP for Vagrant
  config.vm.network :private_network, ip: "10.6.6.6"

  # Brdige to local netowork
  # config.vm.network :public_network

  # Addeitional shares. NFS only work on :private_network
  config.vm.synced_folder "./app", "/var/www/", :nfs => true

  # Up the VB RAM. Default 512MB. 
  # config.vm.provider :virtualbox do |vb|
  #   vb.customize ["modifyvm", :id, "--memory", "1024"]
  # end

  # Provision the VM
  config.vm.provision :shell, :path => "bootstrap.sh"
  
end
