# -*- mode: ruby -*-

Vagrant.configure(2) do |config|
  config.vm.box = "geerlingguy/centos7"
  config.vm.hostname = "repox.vagrant.dev"
  config.vm.network "forwarded_port", guest:8080, host:8080

  config.vm.provision "shell",
    inline: "yum install -y ansible1.9 git; ansible-galaxy install -r /vagrant/requirements.yml"

  config.vm.provision "ansible_local" do |ansible|
    ansible.install = false
    ansible.provisioning_path = "/vagrant"
    ansible.playbook = "vagrant.yml"
  end
end
