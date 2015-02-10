# vim: set filetype=ruby:

Vagrant.configure("2") do |config|
    config.vm.box     = 'vundledemo'
    config.vm.box_url = 'https://oss-binaries.phusionpassenger.com/vagrant/boxes/latest/ubuntu-12.04-amd64-vbox.box'

    config.vm.network 'public_network', bridge: 'wlan0'

    config.vm.provision :shell, inline: "apt-get update"
    config.vm.provision :shell, inline: "apt-get install -y git"

    config.vm.provider "virtualbox" do |providerconf|
        providerconf.name   = 'vundledemo'
        providerconf.memory = 1024
        providerconf.cpus   = 1
    end
end

