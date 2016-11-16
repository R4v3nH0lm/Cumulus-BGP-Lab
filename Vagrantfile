Vagrant.configure("2") do |config|

  config.vm.define "bgp_route_gen" do |bgp_route_gen|
    bgp_route_gen.vm.box = "R4v3nH0lm/IPv4-BGP-Global-Internet-Table"
    bgp_route_gen.vm.provider :virtualbox do |vb|
      vb.name = "bgp_route_gen"
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    bgp_route_gen.vm.hostname = "bgp-route-gen"
    bgp_route_gen.vm.network "private_network", virtualbox__intnet: "swp1", ip: "10.0.0.1"
    # bgp_route_gen.vm.network "private_network", virtualbox__intnet: "swp2"
    # bgp_route_gen.vm.network "private_network", virtualbox__intnet: "swp3"
    # bgp_route_gen.vm.network "private_network", virtualbox__intnet: "swp4"
  end

  config.vm.define "cumulus_ce" do |cumulus_ce|
    cumulus_ce.vm.box = "cumuluscommunity/cumulus-vx"
    cumulus_ce.vm.provider :virtualbox do |vb|
      vb.name = "cumulus_ce"
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    cumulus_ce.vm.hostname = "cumulus-ce"
    cumulus_ce.vm.network "private_network", virtualbox__intnet: "swp1", ip: "10.0.0.2"
    # cumulus_ce.vm.network "private_network", virtualbox__intnet: "swp2"
    # cumulus_ce.vm.network "private_network", virtualbox__intnet: "swp3"
    # cumulus_ce.vm.network "private_network", virtualbox__intnet: "swp4"
  end

end
