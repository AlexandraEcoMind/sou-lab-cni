Vagrant.configure("2") do |config|
  # Nodo soufe1
  config.vm.define "soufe1" do |node|
    node.vm.box = "ubuntu/focal64"
    node.vm.network "private_network", ip: "192.168.1.10"

    # Provision with Ansible
    node.vm.provision "ansible" do |ansible|
      ansible.playbook = "path/to/your/playbook.yml"
      ansible.extra_vars = {
        node_type: "soufe1"
      }
    end

    # Forward port 3000 to access Grafana from the host machine
    node.vm.network "forwarded_port", guest: 3000, host: 3000
  end

  # Nodo soube2
  config.vm.define "soube2" do |node|
    node.vm.box = "ubuntu/focal64"
    node.vm.network "private_network", ip: "192.168.1.20"

    # Provision with Ansible
    node.vm.provision "ansible" do |ansible|
      ansible.playbook = "path/to/your/playbook.yml"
      ansible.extra_vars = {
        node_type: "soube2"
      }
    end
  end
end
