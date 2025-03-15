Vagrant.configure("2") do |config|

    config.vm.define "Jenkins" do |ubuntu|

        ubuntu.vm.box = "bento/ubuntu-24.04"
        ubuntu.vm.box_version = "202502.21.0"
        ubuntu.vm.hostname = "Jenkins"
        config.vm.network "private_network", ip: "192.168.56.10"


        ubuntu.vm.provision "ansible" do |ansible|
            ansible.compatibility_mode = "2.0"
            ansible.playbook = "jenkins/playbook.yml"
        end

        # Change the keyboard layout to French (AZERTY)
        ubuntu.vm.provision "shell", inline: 
        <<-SHELL
            sudo sed -i 's/XKBLAYOUT="us"/XKBLAYOUT="fr"/g' /etc/default/keyboard
            sudo dpkg-reconfigure -f noninteractive keyboard-configuration
            sudo service keyboard-setup restart
        SHELL
    end
  end