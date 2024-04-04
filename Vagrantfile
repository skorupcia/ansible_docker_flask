# -*- mode: ruby -*-
# vi: set ft=ruby :                                 

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # General Vagrant VM configuration.
  config.vm.box = "luminositylabsllc/bento-ubuntu-20.04-arm64"
  config.vm.network :private_network, ip: "192.168.56.39"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", type: "rsync",
    rsync__exclude: ".git/"
  
    config.vm.synced_folder ".", "/vagrant", type: "rsync",
    rsync__exclude: ".git/"
  
  config.vm.hostname = "docker-flask.test"
  config.vm.provider "parallels" do |prl|
    prl.name = "docker-flask.test"
    prl.memory = 1024
    prl.cpus = 2
  end

  #enable provisioning with Ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/main.yml"
  end
end