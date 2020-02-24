Vagrant.configure("2") do |config|
  config.vm.define "virtualbox" do |virtualbox|
    virtualbox.vm.hostname = "centos/7"
    virtualbox.vm.hostname = "mongodb"

    config.vm.provider :virtualbox do |v|
      v.gui = false
      v.memory = 2048
      v.cpus = 2
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--ioapic", "on"]
    end

    config.vm.provision "ansible" 
  end

end