# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define "main" do |main|
    main.vm.box = "ubuntu/trusty64"
    main.vm.network "forwarded_port", guest: 80, host: 10080
    # main.vm.network "private_network", ip: "192.168.33.10"
    # main.vm.network "public_network"
  end


  config.vm.provision "ansible" do |ansible|
    # ansible.groups = {
    #   "test" => ["main"]
    # }
    ansible.playbook = "provisioning/playbook.yml"
  end
end
