# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'chef/ubuntu-14.04'
  config.vm.box_check_update = true
  config.omnibus.chef_version = :latest

  config.vm.provision "chef_solo" do |chef|
    chef.add_recipe "docker"
    chef.add_recipe "packer"

    chef.json = {
      docker: {
        group_members: ['vagrant']
      },
      packer: {
        version: '0.6.0',
        checksum: nil
      }
    }
  end
end
