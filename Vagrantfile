# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # Specify the base box for the VM
  config.vm.box = "generic/ubuntu2204"

  # Configure a public network interface
  config.vm.network "public_network"

  # Disable the default synced folder
  config.vm.synced_folder ".", "/vagrant", disabled: true

  # Configure VirtualBox provider settings
  config.vm.provider "virtualbox" do |vb|
    # Set VM name
    vb.name = "Ubuntu Desktop"
    # Allocate memory
    vb.memory = "4096"
    # Assign CPUs
    vb.cpus = "2"
    # Enable GUI
    vb.gui = true
    # Specify graphics controller
    vb.customize ['modifyvm', :id, '--graphicscontroller', 'vmsvga']
    # Set video RAM size
    vb.customize ['modifyvm', :id, '--vram', '16']
    # Enable bidirectional clipboard sharing
    vb.customize ["modifyvm", :id, "--clipboard-mode", "bidirectional"]
    # Enable bidirectional drag and drop
    vb.customize ["modifyvm", :id, "--draganddrop", "bidirectional"]
    # Configure audio settings: Use DirectSound driver and AC'97 audio controller
    vb.customize ["modifyvm", :id, '--audio', 'dsound', '--audiocontroller', 'ac97']
    
  end

  # Provision the VM with shell script
  config.vm.provision "shell", inline: <<-SHELL
    # Provisioning script
    echo "**** Begin installing Ubuntu, etc"
    sudo apt update 
    sudo apt upgrade -y 
    echo "**** Begin installing ubuntu-desktop"
    sudo apt install ubuntu-desktop -y 
    sudo timedatectl set-timezone Europe/Paris
    echo "**** End installing ubuntu-desktop"
    echo "**** End installing Ubuntu, etc"
  SHELL
end
