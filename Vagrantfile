# -*- mode: ruby -*-
# vi: set ft=ruby :

ENV['VAGRANT_NO_PARALLEL'] = 'yes'

Vagrant.configure(2) do |config|

  NodeCount = 1 #jumlah vm

  (1..NodeCount).each do |i|
    config.vm.define "ubuntuvm1#{i}" do |node|
      node.vm.box = "bento/ubuntu-18.04"
      node.vm.hostname = "ubuntuvm1#{i}.example.com"
      node.vm.network "private_network", ip: "172.42.42.11#{i}"
      node.vm.provider "virtualbox" do |v|
        v.name = "ubuntuvm1#{i}"
        v.memory = 2048
        v.cpus = 2
      end
    end
  end

end
