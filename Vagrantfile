# -*- mode: ruby -*- 
# vi: set ft=ruby : 
Vagrant.configure("2") do |config| 
config.vm.box = "ubuntu/focal64" 
config.vm.define :feg, autostart: false do |feg| 
feg.vm.hostname = "feg" 
feg.vm.network "private_network", ip: "192.168.60.186", nic_type: "82540EM" 
#feg.vm.network "private_network", ip: "192.168.129.84", nic_type: "82540EM" 
feg.vm.provider "virtualbox" do |vb| 
vb.name = "feggw" 
vb.linked_clone = true 
vb.customize ["modifyvm", :id, "--memory", "6144"] 
vb.customize ["modifyvm", :id, "--cpus", "4"] 
vb.customize ["modifyvm", :id, "--nicpromisc2", "allow-all"] 
end 
end 
end 
