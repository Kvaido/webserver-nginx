Vagrant.configure("2") do |config|
    config.vm.box = "centos/7"
 #   config.vm.box = "debian/stretch64"
    config.vm.hostname = "websrv2"
    config.vm.network :private_network, ip: "10.0.0.100"

    config.vm.provider :virtualbox do |vb|
       vb.customize [
         "modifyvm", :id,
         "--memory", "1024",
        ]
    end
	 
 
     config.vm.provision "ansible_local" do |ansible|
     ansible.playbook = "playbook.yml"
	 end
end