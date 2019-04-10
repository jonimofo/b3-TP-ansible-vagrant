# -*- mode: ruby -*-
# =============================================================================
# Nom      : Vagrantfile
# Fonction :
# Usage    :
# Version  : 0.0.1
# vi       : set expandtab shiftwidth=4 softtabstop=4
# =============================================================================
# Quand       Qui      Quoi
# 02/21/19    achiny
# =============================================================================

Vagrant.configure("2") do |centos|

centos.vm.box = "centos/7"

# Disable default synced folder
centos.vm.synced_folder ".", "/vagrant", disabled: true
centos.ssh.insert_key = false

(1..2).each do |i|
  centos.vm.define "node0#{i}" do |config|
      config.vm.hostname = "centos"
      config.vm.network :private_network, ip: "192.168.100.10#{i}"

      config.vm.provider "libvirt" do |libvirt|
        libvirt.memory = 2048
        libvirt.cpus = 1
        libvirt.linked_clone = true
      end
  end
end

end
