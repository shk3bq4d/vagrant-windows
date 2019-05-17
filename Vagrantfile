Vagrant.configure("2") do |config|
  config.vm.box = "mwrock/Windows2016"
#config.vm.customize ["modifyvm", :id, "--memory", 1024]
  config.vm.hostname = "host-win"
  winClientIP = "192.168.99.103"
  config.vm.network "private_network", ip: winClientIP
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 1
	v.linked_clone = true
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "windows.yml"
    ansible.verbose = "vvvvv"
#ansible.raw_arguments = ["-i", "ansible/hostsfile"]
  end

  # Networking
  # config.vm.network :private_network, ip: '192.168.99.12'

  # Shared folder
#config.vm.synced_folder "share", "/vagrant", type: "smb"
end
