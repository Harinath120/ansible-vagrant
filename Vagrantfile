Vagrant.configure("2") do |config|

  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/xenial64"
        ansible.vm.hostname = "ansible"
        ansible.vm.network "private_network", ip: "192.168.1.2"
        ansible.vm.provider "virtualbox" do |vb|
        vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
        end

  end

  config.vm.define "srv01" do |srv01|
  srv01.vm.box = "centos/7"
      srv01.vm.hostname = "srv01"
      srv01.vm.network "private_network", ip: "192.168.1.3"
      srv01.vm.provider "virtualbox" do |vb|
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      vb.memory = "1024"
      vb.cpus = 2
      end

   end

   config.vm.define "srv02" do |srv02|
   srv02.vm.box = "centos/7"
       srv02.vm.hostname = "srv02"
       srv02.vm.network "private_network", ip: "192.168.1.4"
       srv02.vm.provider "virtualbox" do |vb|
       vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
       end

   end

   config.vm.define "srv03" do |srv03|
    srv03.vm.box = "ubuntu/xenial64"
       srv03.vm.hostname = "srv03"
       srv03.vm.network "private_network", ip: "192.168.1.5"
       srv03.vm.provider "virtualbox" do |vb|
       vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
       end
      
   end
end



