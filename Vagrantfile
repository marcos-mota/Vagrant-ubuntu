Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/mantic64"
  config.vm.network "public_network"
  config.vm.synced_folder "site/", "/var/www/html"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "Vagrant-Ubuntu"
    vb.memory = 2048
    vb.cpus = 02
  end
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt install -y nginx
  SHELL
  end
