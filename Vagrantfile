VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "hashicorp/precise32"
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id , "--memory", "512"]
  end

  config.vm.define :db do |db_config|
    db_config.vm.hostname = "db"
    db_config.vm.network :private_network, :ip => "192.168.33.10"
    db_config.vm.provision "ansible" do |ansible|
      ansible.playbook = "db.yml"
    end
  end

  config.vm.define :web do |web_config|
    web_config.vm.hostname = "web"
    web_config.vm.network :private_network,:ip => "192.168.33.12"
    web_config.vm.provision "ansible" do |ansible|
      ansible.playbook = "web.yml"
      ansible.verbose = "vvv"
    end
  end
end

