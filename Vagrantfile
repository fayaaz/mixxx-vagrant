# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.provider "virtualbox" do |v|
    v.memory = 8192
    v.cpus = 4
    v.customize ["modifyvm", :id, "--vram", "128"]
    v.customize ["modifyvm", :id, "--nictype1", "virtio"]
  end

  config.vm.box = "ubuntu/xenial64"

  config.vm.define :MIXXX_BUILD do |t|
  end

  config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end

end