Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise64"

  config.vm.network "private_network", ip: "192.168.33.10" #"internal" lan

  config.vm.network "public_network" #uplink-1
  config.vm.network "public_network" #uplink-2

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
