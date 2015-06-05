# LAMPapp Vagrant

Example usage of [LAMPapp](https://github.com/mbman/lampapp) Chef cookbook

## Requirements

   * [Vagrant 1.5+](http://www.vagrantup.com/)
   * [Virtualbox](https://www.virtualbox.org/) or some other Vagrant provider
   * [ChefDK](http://downloads.getchef.com/chef-dk)
   * Optional: **NFS share** is activated by default for better performance and must me installed on host machine

## How to use

   * Run `sudo vagrant plugin install vagrant-berkshelf && sudo vagrant plugin install vagrant-bindfs` to install neccessary Vagrant plugin
   * Copy [Vagrantfile](./Vagrantfile) and [Berksfile](./Berksfile) files to your project's root dir
   * Set Vagrantile's `chef.lampapp.path` to your project's public web dir
   * Run `vagrant up` to start the VM
   * Your web app is now available at [192.168.56.101](https://192.168.56.101/)
   * Run `vagrant halt` to power off the VM