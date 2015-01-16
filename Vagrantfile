VAGRANTFILE_API_VERSION = "2"

# UTC        	for Universal Coordinated Time
# EST        	for Eastern Standard Time
# US/Central 	for American Central
# US/Eastern 	for American Eastern
# Europe/Madrid	for Europe Madrid

server_timezone  = "UTC"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "ubuntu/trusty64"

    #Установите локальный IP адрес и пропишите в файле hosts (пример: 192.168.33.22 my-project.app) доменное имя для доступа по доменному имени
    #config.vm.network "private_network", ip: "192.168.33.22"

    config.vm.network "forwarded_port", guest: 80, host: 8080
    config.vm.network "forwarded_port", guest: 3306, host: 33060

    config.vm.provider :virtualbox do |vb|
        # Use VBoxManage to customize the VM. For example to change memory:
        vb.customize ["modifyvm", :id, "--memory", "384"]
    end
    # Set share folder permissions to 777 so that apache can write files.
    config.vm.synced_folder ".", "/home/vagrant"
    config.vm.provision :shell, :path => "bootstrap.sh", :args => [server_timezone]
end
