
  Vagrant.configure("2") do |config|
    config.vm.box = "geerlingguy/ubuntu2004"
    config.vm.network "forwarded_port", guest: 3000, host: 3000
    config.vm.network "forwarded_port", guest: 5000, host: 5000
    config.vm.network :private_network, ip: "192.168.56.1"
    #config.vm.network "private_network", type: "dhcp"
    config.vm.hostname = "yolo-app"
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
  
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end
  