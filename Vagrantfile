Vagrant.configure("2") do |config|
   config.vm.provider "docker" do |d|
      d.image = "tknerr/baseimage-ubuntu:18.04"
      d.has_ssh = true
   end
   config.vm.network "forwarded_port", guest: 1880, host: 1880
   config.vm.define 'nodered' do |node|
      node.vm.hostname = 'nodered.local'
      node.vm.provision "ansible" do |ansible|
         ansible.verbose = "v"
         ansible.playbook = "main.yml"
      end
   end
end
