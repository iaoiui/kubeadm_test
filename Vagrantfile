# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = 2
  end

    config.vm.define "controller" do |c|
        c.vm.hostname = "controller"
        c.vm.network "private_network", ip: "10.240.0.1"
        c.vm.provision :shell, :path => "scripts/bootstrap/vagrant-setup-hosts-file.sh"
    end
end
