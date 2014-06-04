# LAMPapp Vagrant

Vagrant setup that runs your web app on Debian Wheezy, with
minimal configuration and all the features provided by Chef cookbooks.

## Requirements

   * [Vagrant 1.5+](http://www.vagrantup.com/)
   * [Virtualbox](https://www.virtualbox.org/) or some other Vagrant provider
   * Optional: **NFS share** is activated by default for better performance and must me installed on host machine

## How to use

   * Clone or unzip this repo into your project's `vagrant/` dir:
   `git clone git@github.com:mbman/lampapp-vagrant.git vagrant`
   * Initialize Chef cookbooks:
   `cd vagrant/ && git submodule update --init --recursive && cd ../`
   * Copy Vagrantfile into project root dir:
   `cp vagrant/Vagrantfile .`
   * Modify Vagrantile's `chef.lampapp.path` to point to your projects public web root
   * Modify Vagrantile's `chef.cookbooks_path = "cookbooks"` to `chef.cookbooks_path = "vagrant/cookbooks"`
   * Run `vagrant up` to start up the VM
   * Your web app is now available at [192.168.56.101](https://192.168.56.101/)
   * Run `vagrant halt` to power off the VM