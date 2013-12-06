# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  
  # use a Ubuntu 12.04 box
  # 
  config.vm.box = "precise64"
  config.vm.box_url = 'http://files.vagrantup.com/precise64.box'
  
  # make VM's port 80 addressable as http://localhost:8080 
  # 
  config.vm.network :forwarded_port, guest: 80, host: 8080
  
  
  # assign an IP to the VM so we can come back and run ansible
  # it apart from the vagrant provisioning process.
  # 
  # this IP matches the IP in the hosts file
  #
  config.vm.network :private_network, ip: "192.168.56.10"
  
  
  # provision the VM with the server-nodejs ansible file
  # 
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "server-nodejs.yml"
    ansible.inventory_path = "hosts"
  end
end
