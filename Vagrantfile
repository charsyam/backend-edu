Vagrant.configure(2) do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
    v.customize ["setextradata", :id, "VBoxInternal2/SharedFoldersEnableSymlinksCreate/v-root", "1"]
  end
  config.vm.define "vm1" do |vm1|
    vm1.vm.box = "charsyam/backend-basics-18.04"
    vm1.vm.network :private_network, ip: "192.168.50.5"
  end
  config.ssh.username = "vagrant"
  config.ssh.password = "vagrant"
end
