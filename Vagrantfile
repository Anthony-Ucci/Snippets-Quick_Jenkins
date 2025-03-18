Vagrant.configure("2") do |config|

    config.vm.define "Jenkins" do |ubuntu|

        ubuntu.vm.box = "bento/ubuntu-24.04"
        ubuntu.vm.box_version = "202502.21.0"
        ubuntu.vm.hostname = "Jenkins"
        ubuntu.vm.network "private_network", ip: "192.168.56.10"

        ubuntu.vm.provider "virtualbox" do |vb|
            vb.name = "Jenkins"
            vb.memory = 1024
            vb.cpus = 2
        end

        ubuntu.vm.provision "ansible" do |ansible|
            ansible.compatibility_mode = "2.0"
            ansible.playbook = "playbook.yml"
        end
    end
  end
