Vagrant.configure("2") do |centos|

centos.vm.box = "centos/7"

# Disable default synced folder
centos.vm.synced_folder ".", "/vagrant", disabled: true
centos.ssh.insert_key = false

# centos - web
centos.vm.define "web" do |config|
  config.vm.hostname = "web"
  config.vm.network :private_network, ip: "192.168.200.201"
  config.vm.provider "libvirt" do |libvirt|
    libvirt.memory = 2048
    libvirt.cpus = 1
    libvirt.linked_clone = true
  end
end

# centos - mysql
centos.vm.define "mysql" do |config|
  config.vm.hostname = "mysql"
  config.vm.network :private_network, ip: "192.168.200.202"
  config.vm.provider "libvirt" do |libvirt|
    libvirt.memory = 2048
    libvirt.cpus = 1
    libvirt.linked_clone = true
  end
end

end
