Vagrant LAMP
============
[Описание на русском](https://github.com/SidiGi/vagrant-lamp/blob/master/README.ru.md)

My default LAMP development stack configuration for Vagrant.

Requirements
------------
* VirtualBox <http://www.virtualbox.com>
* Vagrant <http://www.vagrantup.com>
* Git <http://git-scm.com/>

Use
-----
### Begin
	$ git clone https://github.com/SidiGi/vagrant-lamp.git
	$ vagrant up


### Connection

#### Apache 2
Apache 2 is available on <http://localhost:8080>

#### phpMyAdmin
phpMyAdmin is available on <http://localhost:8080/phpmyadmin/>
```js
	login: vagrant
	password: vagrant
```

#### MySQL
MySQL server is available on `33060` port , and on `3306` in VM.
```js
	login: vagrant
	password: vagrant
```

Technical description
-----------------
* Ubuntu 14.04 64-bit
* phpMyAdmin 4.0
* Apache 2.4.7
* PHP 5.5
* MySQL 5.5
* NPM (optional)
* NodeJS (optional)
* Composer (optional)
* Gulp (optional)
* Bower (optional)

This project uses a basic package of Ubuntu 14.04 x64 (VagrantCloud). If you have not downloaded the file box, then the first time you install will download the necessary box (soderzhatsy a necessary packages for the operating system).

The root folder of the site is located in the project folder and is called the `public`. You can create your files in it.

#### Vagrant
You can connect to the virtual machine Vagrant command (password vagrant)
```js
	$ vagrant ssh
```

#### MySQL
mysql not accessible via ssh connection (vagrant ssh)