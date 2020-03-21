
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |v|
	v.memory = 2048
  end

  config.vm.define "postgres" do |m|
	m.vm.network "private_network", ip: "172.17.177.42"
  end

  config.vm.define "service-register" do |m|
	m.vm.network "private_network", ip: "172.17.177.40"
  end

end
