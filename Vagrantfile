# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "precise"
  config.vm.forward_port 8080, 8080

  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = ["."]
    chef.add_recipe("jenkins")
  end
end
