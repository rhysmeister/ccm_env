Vagrant.configure("2") do |config|
    config.vm.box = "bento/ubuntu-20.04"
    config.vm.synced_folder ".", "/vagrant", disabled: true
    node_name = "ccm"
    config.vm.define node_name do |node|
        node.vm.hostname = node_name
    end
    config.vm.provider "virtualbox" do |v|
        v.memory = 4092
    end

    config.vm.provision :ansible do |ansible|
        ansible.limit = "all"
        ansible.become = true
        ansible.playbook = "ccm.yml"
      end
  end