LAMPapp Vagrant
===============

Vagrant setup that runs your local project on LAMP server with minimal config.

Your project is available on **192.168.56.101** IP (`*.vagrant.dev` alias)
and you can connect to MySQL remotely using the same IP as **root::foobar**


This is an example usage of **LAMPapp Vagrant Chef** cookbook:

  https://github.com/mbman/lampapp

Requirements
------------

  http://www.vagrantup.com/

- **NFS share** is activated by default for better performance and must me installed on host machine (windows not supported).
- ***Chef cookbook dependencies** are included as git submodules and need to be initialized.

Setup
-----

1.  Clone or unzip this repo into your project's `vagrant/` dir

2.  Recursively `git submodule init` & `git submodule update` all `vagrant/` and `vagrant/cookbooks/` git submodules

3.  Copy `vagrant/Vagranfile` to your project root and change values

4.  `chef.cookbooks_path` - path to cookbooks dir (`vagrant/cookbooks/`)
    
5.  `chef.lampapp.path` - relative path to public directory

6.  Run `vagrant up` from your project root


Your project is now running on a LAMP server and can be access using
the static IP address (modify your `hosts` file for domain usage), with or without SSL:
    
- http://192.168.56.101 
- https://192.168.56.101 
- http(s)://vagrant.dev
- http(s)://www.vagrant.dev
- http(s)://*.vagrant.dev