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
