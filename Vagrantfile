Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2004"
  config.vm.network "private_network", type: "dhcp"

#VirtualBox configuration
  config.vm.provider "virtualbox" do |v|
    v.name = "Ubuntu"
    v.memory = 2560
  end

#Provisioning ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "Ansible/myplaybook.yml"
  end

end