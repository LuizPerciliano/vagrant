# Grab the name of the default interface
#$default_network_interface = `ip route | awk '/^default/ {printf "%s", $5; exit 0}'`

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 8090
  #config.vm.network "public_network", ip: "192.168.1.24"
  config.vm.network "public_network", bridge: "Realtek PCIe GbE Family Controller #2", ip: "192.168.1.24"
end
