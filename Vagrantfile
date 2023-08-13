# -*- mode: ruby -*-
# vi: set ft=ruby :
# Before execute this Vagrant File, Type the command below in your Linux Terminal
#   export VAGRANT_EXPERIMENTAL="disks"

Vagrant.configure("2") do |config|
    config.vm.box = "roboxes/ubuntu2204"
    
    config.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory = "1024"
    end
  
    #
    # Configurations of Student VM
    #
    config.vm.define "Ubuntu22-SOA-Server01" do |aluno|
      aluno.vm.hostname = "Ubuntu22-SOA-Server01"
      aluno.vm.network "private_network", ip: "192.168.57.25"
      aluno.vm.network "public_network", bridge: "enp2s0"
  
      aluno.vm.provider "virtualbox" do |vb|
        vb.name = "Ubuntu22-SOA-Server01"
      end

      (0..3).each do |i|
        aluno.vm.disk :disk, size: "10GB", name: "disk-#{i}"
      end
    end # End conf do aluno
end
  
