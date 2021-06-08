# DevEnvironment

## Vagrantfile Setup

Create a vagrant file with the following contents:
```
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64" 
  config.vm.network "private_network", ip: "192.168.10.100"
  
  end
```

## Vagrant Commands
- To launch the VM: `vagrant up`
- To close the VM and clean up all the resources: `vagrant destroy`
- To view VM status: `vagrant status`
- To access the running VM: `vagrant ssh`
- To suspend the VM: `vagrant suspend`

## VM Commands
After using the `vagrant ssh` command:
- To update the VM: `sudo apt-get update -y`
- To install a specific program: `sudo apt-get install [program name]`
- To install nginx specifically: `sudo apt-get install nginx`
- To exit the VM: `exit`

## Verify Nginx
- Open a browser and enter `192.168.10.100` into the URL window
- A "Welcome to nginx" splash page should be visible.
