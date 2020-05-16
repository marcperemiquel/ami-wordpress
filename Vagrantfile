# Local dev

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.hostname = "ago-moodle-box"

  config.vm.provider "virtualbox" do |v|
        v.name = "AGO - Portal Box"
        v.customize ["modifyvm", :id, "--cpus", '1']
        v.customize ["modifyvm", :id, "--memory", '2048']
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.compatibility_mode = '2.0'
    ansible.limit = 'all'
    ansible.inventory_path = 'hosts'
    ansible.playbook = 'playbook-local.yml'
  end

end
