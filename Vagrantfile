Vagrant.configure("2") do |config|
  config.vm.define "etcd01" do |etcd01|
    etcd01.vm.box = "generic/oracle9"
    etcd01.vm.hostname = "etcd01"
    etcd01.vm.network "private_network", ip: "172.16.100.11"
    etcd01.vm.network "forwarded_port", guest: 5432, host: 5432
    etcd01.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 2
    end
  end
  config.vm.define "pgsql01" do |pgsql01|
    pgsql01.vm.box = "generic/oracle9"
    pgsql01.vm.hostname = "pgsql01"
    pgsql01.vm.network "private_network", ip: "172.16.100.12"
    pgsql01.vm.network "forwarded_port", guest: 5432, host: 6432
    pgsql01.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 2
    end
  end
  config.vm.define "pgsql02" do |pgsql02|
    pgsql02.vm.box = "generic/oracle9"
    pgsql02.vm.hostname = "pgsql02"
    pgsql02.vm.network "private_network", ip: "172.16.100.13"
    pgsql02.vm.network "forwarded_port", guest: 5432, host: 7432
    pgsql02.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 2
    end
  end
  config.vm.define "k3s01" do |k3s01|
    k3s01.vm.box = "generic/oracle9"
    k3s01.vm.hostname = "k3s01"
    k3s01.vm.network "private_network", ip: "172.16.100.14"
    k3s01.vm.network "forwarded_port", guest: 80, host: 80
    k3s01.vm.network "forwarded_port", guest: 443, host: 443
    k3s01.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end
end