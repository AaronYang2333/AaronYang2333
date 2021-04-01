---
title: use vagrant to create vm instance
catalog: true
mathjax: false
date: 2021-03-27 02:49:13
subtitle:
header-img:
tags:
- Vagrant
- Virtual Instance
- Steup
categories:
- Vagrant
---

### Steps
0. goto "https://app.vagrantup.com/boxes/search", and find box you wanna install.
	E.G. I wanna install ubuntu 14 image.

1. make a dir "vagrant-ubuntu-14" on local machine.
  <img src="1.png"  style="display:inline;box-shadow: none !important;">

2. open git bash in here, and execute "vagrant init ubuntu/trusty64".
  <img src="2.png"  style="display:inline;box-shadow: none !important;">

3. got a file named "Vagrantfile"
  <img src="3.png"  style="display:inline;box-shadow: none !important;">

4. use same git bash and execute "vagrant up".
	make sure you have the "Vagrantfile" file at your current path.
  <img src="4.png"  style="display:inline;box-shadow: none !important;">

5. a dir named ".vagrant" appeared.
	"\.vagrant\machines\default\virtualbox" saved your private key, which you can use to connect your virtual image from third-party terminal.
  <img src="5.png"  style="display:inline;box-shadow: none !important;">

### Customize your vagrant file
```ruby
# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  # 镜像源设置
  config.vm.box = "ubuntu/xenial64"

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # 每次启动，需不需要跟镜像源去比较，可能触发更新
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # 端口转发规则
  config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # 固定内网IP
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # 固定公网IP
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # 共享文件夹设置
  config.vm.synced_folder "./local_data", "/vm_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    # vb.gui = true
  
    # Customize the amount of memory on the VM:
    # 内存及核心数
    vb.memory = "2048"
    vb.cpus = 2
  end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # 当VM启动时，需要执行的命令
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end

```

### Tips：

1. reload VM

```shell
vagrant reload
```

