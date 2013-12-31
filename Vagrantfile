# -*- mode: ruby -*-
# vi: set ft=ruby :
# This is a Vagrant configuration file. It can be used to set up and manage
# virtual machines on your local system or in the cloud. See http://downloads.vagrantup.com/
# for downloads and installation instructions, and see http://docs.vagrantup.com/v2/
# for more information and configuring and using Vagrant.

Vagrant.configure("2") do |config|

  config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.box = "opscode-ubuntu-12.04-i386"
    ubuntu.vm.box_url = "https://opscode-vm.s3.amazonaws.com/vagrant/opscode_ubuntu-12.04-i386_provisionerless.box"
    ubuntu.vm.hostname = "ubuntu-target"
    ubuntu.vm.network :forwarded_port, guest: 80, host: 8080
  end

  config.vm.define "centos" do |centos|
    centos.vm.box = "opscode_centos-6.4"
    centos.vm.box_url = "https://opscode-vm-bento.s3.amazonaws.com/vagrant/opscode_centos-6.4_provisionerless.box"
    centos.vm.hostname = "centos-target"
    centos.vm.network :forwarded_port, guest: 80, host: 8081
  end
end
