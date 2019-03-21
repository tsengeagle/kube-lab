# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.provider "virtualbox" do |vb|
    vb.cpus=2
    vb.memory=1024
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision.yml"
  end
  # config.vm.provision "shell", inline: <<-SHELL
  #   sudo yum install -y yum-utils device-mapper-persistent-data lvm2
  #   sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
  #   sudo yum install -y docker-ce docker-ce-cli containerd.io
  #   sudo usermod -aG docker vagrant
  #   sudo systemctl start docker
  #   curl https://copr-be.cloud.fedoraproject.org/results/ganto/lxd/epel-7-x86_64/00486278-lxcfs/lxcfs-2.0.5-3.el7.centos.x86_64.rpm -o /tmp/lxcfs-2.0.5-3.el7.centos.x86_64.rpm
  #   sudo yum install -y /tmp/lxcfs-2.0.5-3.el7.centos.x86_64.rpm
  #   sudo systemctl start lxcfs

  # SHELL
end
