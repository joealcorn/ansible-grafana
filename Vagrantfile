# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "grafana" do |grafana|
    grafana.vm.box = "ubuntu/trusty64"
    grafana.vm.network :private_network, ip: "192.168.33.22"

    grafana.vm.provision "ansible" do |ansible|
      ansible.playbook = "grafana.yml"
    end
  end
end
