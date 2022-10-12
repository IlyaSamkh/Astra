Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2004"
#Private network
  config.vm.network "private_network", type: "dhcp"
#Forwarded ports
  config.vm.network "forwarded_port", guest: 3000, host: 3000

#VirtualBox configuration
  config.vm.provider "virtualbox" do |v|
    v.name = "Ubuntu"
    v.memory = 4096
  end

#Provisioning ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "Ansible/myplaybook.yml"
  end

end