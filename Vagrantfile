# -*- mode: ruby -*-
# vi: set ft=ruby :



Vagrant.configure(2) do |config|

   config.vm.box = "ubuntu/trusty64"

  config.vm.define "db", primary: true do |db|

      db.vm.provider :virtualbox do |vb|

          vb.gui = false

          vb.customize ["modifyvm", :id, "--memory", "1024"]
      end

      db.vm.network :private_network, ip: '192.168.68.5'


      db.vm.provision :docker, run: :always do |docker|

        docker.build_image "/vagrant/good",
            args: "-t good"

        docker.build_image "/vagrant/bad",
            args: "-t bad"

        docker.run "good"

        docker.run "bad"
      end
  end

end