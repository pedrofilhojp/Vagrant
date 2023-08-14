# Vagrant

In this repository, i'm shared with my students files and main commands lines used in our Linux Server Course that we will cover:
- Use Vagrant to build our Linux Envoironment;
- Linux Administrator with Ansible;
- Basics about Hardening Linux Server;
- Disc Management: RAID, LVM, Linux Partitions...
- Transfer File: SFTP, FTP, SMB and NFS Services
- Name Resolution (DNS Service with Bind9)
- Webserver Apache ( Virtualhost, security, https, authentication, error pages...)
- Webserver Nginx ( Virtualhost, Proxy, LoadBalance, Error Pages...)
- DHCP Service
- Domain Controler ( Samba4 )
- Firewall Proxy Squid
- Firewall UTM - PFSense

## Install Vagrant
Use the information available in Official documentation of Vagrant
> https://developer.hashicorp.com/vagrant/docs/installation

## How does works Vagrant
Vagrant its the Hashcorp solution to provision virtualization infraestructure to VirtualBox, VMware, Hyperv...

- 1º **BOX:** You need to specify the Box that you will use

  This box, after downloaded will be store inside your home directory on path "~/.vagrant.d/boxes".
  You can see all Box available in: https://app.vagrantup.com/boxes/search
  
- 2º **Provider:** Tell to Vagrant which the virtualization solution will be used, VirtualBox, Vmware...
- 3º **Configure VM:** If you need, can to customize the virtual machine, network, gui, total memory...
- 4º **Provision:** You can too execute scripts, or call specialize software to configure the system, how Puppet, Ansible, Chef...


## Main commands line that i use

- **vagrant init**: Creating initial Vagrantfile. If you dont know how to start, you can execute this command. But don't worry, we will use the "Vagrantfile" file shared in this repository for all our classes.
  
- **vagrant box list**: Show the boxes dowloaded in you system

The commands below, will read the configurations inside the Vagrantfile, therefore, need to execute in same path.
- **vagrant up**: Will **start** or **create** the virtual machines
- **vagrant ssh [virtual machine name]**: Normally, all box is builded with ssh key-pairs. After start the VM based in any box, With this command, you can access the VM using private ssh key that is store in .vagrant directory in same path of Vagrantfile.
- **vagrant halt**: Stop all VM inside the Vagrantfile
- **vagrant status**: Verify status of all VMs
- **vagrant reload**: Restart the VMs
- **vagrant destroy**: Stop and delete all VMs

