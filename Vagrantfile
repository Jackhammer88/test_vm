Vagrant.configure("2") do |config|
  config.vm.box = "madfisht3/ubuntu-focal-linux-6"
  config.vm.box_version = "1"
  config.vm.define "otus-hw1"

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
    vb.cpus = "1"
  end

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y apache2
  SHELL
end
