Vagrant.configure("2") do |config|
if Vagrant.has_plugin? "vagrant-vbguest"
	config.vbguest.no_install = true
	config.vbguest.auto_update = false
	config.vbguest.no_remote = true
end
	config.vm.define :streama do |streama|
		streama.vm.box = "bento/centos-7"
		streama.vm.network :private_network, ip: "192.168.50.2"
		streama.vm.hostname = "streama"
    end
	config.vm.define :firewall do |firewall|
		firewall.vm.box = "bento/centos-7"
		firewall.vm.network :private_network, ip: "192.168.50.4"
		firewall.vm.network :public_network, use_dhcp_assigned_default_route: true
		firewall.vm.hostname = "firewall"
    end
end
