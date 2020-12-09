# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "windows10"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/domain.yaml"
    ansible.extra_vars = {
        domain_name: ENV['VG_DOMAIN_NAME']
        domain_admin: ENV['VG_DOMAIN_ADMIN']
        domain_pass: ENV['VG_DOMAIN_PASS']        
    }
  end
end
