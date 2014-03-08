Vagrant.configure("2") do |config|
  config.vm.box = "raring64"
  config.vm.box_url = "http://goo.gl/Y4aRr"

  (49000..49005).each do |port|
    config.vm.network "forwarded_port", guest: port, host: port
  end
  
  config.vm.provision "shell", path: "install_docker.sh"

  config.vm.synced_folder "data", "/data"
end