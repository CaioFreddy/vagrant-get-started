$script = <<SCRIPT
apt update && apt install -y nginx
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 8089
  config.vm.network "public_network"
  config.vm.provision "shell", inline: "echo Hello, World"
end
