# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.box = "ferventcoder/win7pro-x64-nocm-lite"

    config.vm.box_check_update = false
    config.vm.network "forwarded_port", guest: 4444, host: 4446
    config.vm.guest = :windows
    config.ssh.insert_key = false
    config.vm.synced_folder '.', '/vagrant'

    # config.vm.provision :shell, path: "bootstrap.ps1"     # (see #1)

    config.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
        vb.cpus = "1"
    end
end
