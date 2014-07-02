# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.hostname = "ldap-self-service"

  config.vm.box = "ubuntu/trusty64"
  config.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
  end

  config.vm.network :forwarded_port, guest: 8080, host: 9070
  config.vm.network "private_network", ip: "192.168.50.5"

  config.vm.provision "ansible" do |ansible|
    #ansible.verbose = "vvvv"
    #ansible.tags=["tag"]
    ansible.playbook = "provisioning/servers.yml"
  end

end
