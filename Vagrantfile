Vagrant.configure("2") do |config|

  config.vm.define "bgp1" do |bgp1|
    bgp1.vm.box = "R4v3nH0lm/IPv4-BGP-Global-Internet-Table"
    bgp1.vm.provider :virtualbox do |vb|
      vb.name = "bgp1"
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    bgp1.vm.hostname = "bgp1"
    bgp1.vm.network "private_network", virtualbox__intnet: "swp1"
    # bgp1.vm.network "private_network", virtualbox__intnet: "swp2"
    # bgp1.vm.network "private_network", virtualbox__intnet: "swp3"
    # bgp1.vm.network "private_network", virtualbox__intnet: "swp4"
  end

end
