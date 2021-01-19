Vagrant.configure(2) do |config|
	config.vm.define "devops-box" do |devbox|
		devbox.vm.box = "ubuntu/bionic64"
    		#devbox.vm.network "private_network", ip: "192.168.199.9"
    		#devbox.vm.hostname = "devops-box"
      		devbox.vm.provision "shell", path: "scripts/install.sh"
			devbox.vm.provision "shell", inline: " mkdir ~/scripts"				  
			devbox.vm.provision "file", source: "./scripts/install_azure_cli.sh", destination: "~/scripts/install_azure_cli.sh"   
    		devbox.vm.provider "virtualbox" do |v|
    		  v.memory = 4096
    		  v.cpus = 2
    		end
	end
end
