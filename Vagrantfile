# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
    
  config.vm.define "master" do |m|
    m.vm.box = "geerlingguy/ubuntu2004"
    m.vm.network "private_network", ip: "192.168.60.10"
    m.vm.network "forwarded_port", guest: 3030, host: 3030
    m.vm.hostname = "master"

    m.vm.provider :virtualbox do |vb|
      vb.name = "speedtest"
      vb.memory = 2048
      vb.cpus = 2
      vb.check_guest_additions = false 
    end 
  end  
end
