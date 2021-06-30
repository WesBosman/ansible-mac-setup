Vagrant.configure("2") do |config|
    config.vm.box = "ashiq/osx-10.14"
    config.vm.box_version = "0.1"
    
    config.vm.network "private_network", ip: "192.168.50.4"
    
    config.ssh.forward_agent = true

    config.vm.boot_timeout = 300

    config.vm.synced_folder ".", "/vagrant", disabled: true

    config.vm.provider "virtualbox" do |vb|
        vb.check_guest_additions = false
    end

    config.vm.provision :ansible do | ansible | 
        # ansible.host_key_checking = false
        # ansible.ask_vault_pass = false
        ansible.playbook = "main.yml"
        ansible.inventory_path = "local"
        ansible.limit = "all"
        ansible.verbose = "v"
    end
end