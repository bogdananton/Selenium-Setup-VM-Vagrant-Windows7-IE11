# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.box = "ferventcoder/win7pro-x64-nocm-lite"

    config.vm.box_check_update = false
    config.vm.network "forwarded_port", guest: 4444, host: 4446
    config.vm.guest = :windows
    config.ssh.insert_key = false
    config.vm.synced_folder '.', '/vagrant'

#    Until this will be available, provision manually by running bootstrap.ps1
#    config.vm.provision 'shell' do |s|
#        s.inline = 'copy \\VBOXSVR\vagrant\bootstrap.ps1 c:\bootstrap.ps1; powershell -NonInteractive -File c:\bootstrap.ps1'
#    end

    config.vm.provider "virtualbox" do |vb|
        vb.gui = true
        vb.memory = "1024"
        vb.cpus = "1"
    end

    config.push.define "atlas" do |push|
        push.app = "bogdananton/Selenium-Setup-VM-Win7-IE11"
    end
end

