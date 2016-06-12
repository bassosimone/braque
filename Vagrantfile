Vagrant.configure(2) do |config|
  config.vm.synced_folder ".", "/braque"
  config.vm.define "trusty64" do |trusty64|
    trusty64.vm.box = "ubuntu/trusty64"
    trusty64.vm.provider "virtualbox" do |v|
      v.memory = 4096
      v.cpus = 4
    end
    trusty64.vm.provision "shell", inline: <<-SHELL
      cd /braque
      ./usr/lib/braque/provision-trusty64
    SHELL
  end
end
