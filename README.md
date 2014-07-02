## Get started with one line, using Vagrant

The three prerequisites, which are available on Mac, Windows, and Linux 
are (we have tested with the versions below, but other versions may be fine too):

1. [VirtualBox 4.3.12](https://www.virtualbox.org/wiki/Downloads)
2. [Vagrant 1.6.2](http://www.vagrantup.com/downloads)
3. [Ansible 1.6.1](http://docs.ansible.com/intro_installation.html)

Once you have Virtualbox and Vagrant installed on your machine, you can:

```
vagrant plugin install vagrant-vbguest
git clone https://github.com/smart-on-fhir/installer-service
cd installer
vagrant up
```

... wait ~10min while everything installs (depending on your Internet connection speed).

Now visit `http://localhost:9070` in a web browser on your local ("host") machine.