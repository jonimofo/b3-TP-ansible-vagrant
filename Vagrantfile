Vagrant.configure("2") do |ubuntu|

ubuntu.vm.box = "bento/ubuntu-18.04"

# Disable default synced folder
ubuntu.vm.synced_folder ".", "/vagrant", disabled: true
ubuntu.ssh.insert_key = false

# Ubuntu - web
ubuntu.vm.define "web" do |config|
  config.vm.hostname = "web"
  config.vm.network :private_network, ip: "192.168.200.101"
  config.vm.provider "libvirt" do |libvirt|
    libvirt.memory = 2048
    libvirt.cpus = 1
    libvirt.linked_clone = true
  end
end

# Ubuntu - mysql
ubuntu.vm.define "mysql" do |config|
  config.vm.hostname = "mysql"
  config.vm.network :private_network, ip: "192.168.200.102"
  config.vm.provider "libvirt" do |libvirt|
    libvirt.memory = 2048
    libvirt.cpus = 1
    libvirt.linked_clone = true
  end
end

end
