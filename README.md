LAMPapp Vagrant
===============

Vagrant setup that runs your local project on LAMP server with minimal config.

Your project is available on 192.168.56.101 IP (*.vagrant.dev alias)
and you can connect to MySQL remotely using the same IP as root:foobar


This is an example for LAMPapp Vagrant Chef cookbook:

    https://github.com/mbman/lampapp

REQUIREMENTS
============

  - http://www.vagrantup.com/

SETUP
=====

  - Clone, fork or unzip this repo into your project root
  - Initialize all cookbook submodules
  - Run "vagrant up" from project root

Your project is now running on a LAMP server and can be access using
the static IP address, with or withour SSL:
    
    http://192.168.56.101 
    https://192.168.56.101 