# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.define "ruby" do |ruby|
      ruby.vm.box = "ubuntu/trusty64"
      ruby.vm.hostname = "ruby"
      ruby.vm.network "private_network", ip: "192.168.88.10"
  end
 
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "tests/test.yml"
    ansible.inventory_path = "tests/inventory"
  end

end
