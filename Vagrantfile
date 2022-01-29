
Vagrant.configure("2") do |config|
  config.vm.define "skillbox_vagrant"
  config.vm.box = "ubuntu/trusty64"

  config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"
  
  config.vm.provision "shell", privileged: false, inline: <<-SHELL
#Requirements
sudo apt-get -y install make
sudo apt-get -y install gcc
sudo apt-get -y install libreadline6 libreadline6-dev
sudo apt-get -y install zlib1g-dev
sudo apt-get -y install bison

#Download postgres
wget http://ftp.postgresql.org/pub/source/v8.4.22/postgresql-8.4.22.tar.gz
tar xfz postgresql-8.4.22.tar.gz
cd postgresql-8.4.22

./configure
 
 
 SHELL
end
