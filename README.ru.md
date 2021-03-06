Vagrant-lamp. Веб окружение для разработчика (LAMP), разработанное на основе Vagrant.
============

Vagrant-lamp позволяет развернуть рабочую среду одной коммандой с установленными инструментами и базовыми настройками.

Среда

Требования
------------
* VirtualBox <http://www.virtualbox.com>
* Vagrant <http://www.vagrantup.com>
* Git <http://git-scm.com/>

Использование
-----
### Начало
	$ git clone https://github.com/SidiGi/vagrant-lamp.git
	$ cd vagrant-lamp
	$ vagrant up


### Соединение

#### Apache
Апач доступен по адресу <http://localhost:8080>

#### phpMyAdmin
phpMyAdmin доступен по адресу <http://localhost:8080/phpmyadmin/>
```js
	Логин: vagrant
	Пароль: vagrant
```

#### MySQL
MySQL сервер доступен по порту `33060`, при запуске виртуальной машины он доступен по стандартному порту `3306`.
```js
	Логин: vagrant
	Пароль: vagrant
```

Техническое описание
-----------------
* Ubuntu 14.04 64-bit
* phpMyAdmin 4.0
* Apache 2.4.7
* PHP 5.5
* MySQL 5.5
* NPM (опционально)
* NodeJS (опционально)
* Composer (опционально)
* Gulp (опционально)
* Bower (опционально)

В данном проекте используются базовый пакет Ubuntu 14.04 x64 (VagrantCloud). Если у вас не загружен box файл, то в первый раз при установке будет загружен необходимый box (содержаций в себе необходимые пакеты для работы ОС).

Корневая папка сайта расположена в папке проекта и называется `public`. Вы можете создавать свои файлы в ней.

#### Vagrant
Вы можете подключится к виртуальной машине Vagrant через команду (пароль vagrant)
```js
	$ vagrant ssh
```

#### MySQL
mysql недоступен через ssh соединение (vagrant ssh)
