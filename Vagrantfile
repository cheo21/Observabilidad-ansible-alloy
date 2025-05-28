Vagrant.configure("2") do |config|
    config.vm.box = "alvistack/rhel-9"
    config.vm.network "private_network", type: "dhcp"
    config.vm.network "forwarded_port", guest: 12345, host: 12345, host_ip:"127.0.0.1"
    config.vm.provider :libvirt do |libvirt|
      libvirt.memory = 4096
      libvirt.cpus = 2
    end
  
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end
 