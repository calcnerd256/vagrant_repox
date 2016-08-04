# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "geerlingguy/centos7"
  config.vm.hostname = "repox.vagrant.dev"
  config.vm.network "forwarded_port", guest:8080, host:8080
  # We use a shell provisioner instead of an Ansible provisioner because of Windows
  config.vm.provision "shell",
    path: "bootstrap.sh", keep_color: "True"
end
