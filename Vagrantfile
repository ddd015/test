# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
    config.vm.box = "debian/buster64"
    config.vm.network "forwarded_port", guest: 80, host: 80  
    config.vm.define "test" do |test|
        test.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "playbook.yaml"
        ansible.become = true
      end
    end
  end