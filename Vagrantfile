Vagrant.configure("2") do |config|
  # Nodo soufe1
  config.vm.define "soufe1" do |node|
    node.vm.box = "ubuntu/focal64"
    node.vm.network "private_network", ip: "192.168.1.10"
  end

  # Nodo soube2
  config.vm.define "soube2" do |node|
    node.vm.box = "ubuntu/focal64"
    node.vm.network "private_network", ip: "192.168.1.20"
  end
end
