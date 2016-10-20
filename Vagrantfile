# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "bento/centos-7.2"

  config.vm.define "server1", primary: true do |server1|
    server1.vm.network "private_network", ip: "192.168.1.2", virtualbox__intnet: "fm_local_network"
    server1.vm.network "forwarded_port", guest: 22, host: 1022, id: "ssh"
  end

  config.vm.define "server2", primary: true do |server2|
    server2.vm.network "private_network", ip: "192.168.1.3", virtualbox__intnet: "fm_local_network"
    server2.vm.network "forwarded_port", guest: 22, host: 2022, id: "ssh"
  end
end
