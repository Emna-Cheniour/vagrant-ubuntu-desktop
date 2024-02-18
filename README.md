# vagrant-ubuntu-desktop
This repository contains a Vagrantfile configured to create a Ubuntu Desktop virtual machine using Vagrant and VirtualBox. The VM is pre-configured with Ubuntu 20.04, GUI interface, and other customizations for development purposes.

## Prerequisites
Before using this Vagrantfile to create a virtual machine, ensure you have the following installed:
- [Vagrant](https://developer.hashicorp.com/vagrant/downloads)
- [VirtualBox](https://download.virtualbox.org/virtualbox/7.0.14/VirtualBox-7.0.14-161095-Win.exe)

## Getting Started
1. Clone or download the Vagrantfile provided in this repository.

2. Open a terminal and navigate to the directory containing the Vagrantfile.

3. Run the following command to create and configure the virtual machine:<br>
<span style="color:red">some **vagrant up** text</span>

4.Once the VM is created, you can access it either via SSH using the command <span style="color:red">some **vagrant ssh** text</span> in your terminal, or directly through the VirtualBox window interface.
_Note: Once installed, the VM can be accessed and managed anytime via the VirtualBox interface._

5. The default username and password for the VM are both `vagrant`.

6. To stop the virtual machine, use:<br>
<span style="color:red">some **vagrant halt** text</span>

7. To completely remove the virtual machine, run:<br>
<span style="color:red">some **vagrant destroy** text</span>

## Vagrantfile Configuration
- The Vagrantfile is pre-configured to use the `generic/ubuntu2204` base box.
- It allocates 4096 MB of memory and 2 CPUs to the VM.
- GUI is enabled for the VM, allowing you to interact with it visually.
- Bidirectional clipboard sharing and drag-and-drop functionalities are enabled between the host and guest systems.

## Provisioning
The Vagrantfile includes a provisioning script that installs Ubuntu Desktop and sets the timezone to Europe/Paris. You can customize the provisioning script to suit your requirements.

## Notes
- Make sure to adjust resource allocations and configurations as needed for your environment.
- Feel free to modify the Vagrantfile to meet your specific use case or requirements.
