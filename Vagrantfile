# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "boxcutter/centos68"
  config.vm.box_version = "2.0.16"

  if Vagrant.has_plugin?("vagrant-cachier")
    config.cache.scope = :box
    config.cache.synced_folder_opts = {
        type: :virtualbox
      }
  end

  boxes = [
    {
      :hostname => "redis1",
      :ip => "192.168.33.10"
    },
    {
      :hostname => "redis2",
      :ip => "192.168.33.11"
    },
    {
      :hostname => "redis3",
      :ip => "192.168.33.12"
    }
  ]

  boxes.each do |machine|
    config.vm.define machine[:hostname] do |node|
      node.vm.hostname = machine[:hostname]
      node.vm.network "private_network", ip: machine[:ip]
    end
  end
end
