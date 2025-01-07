Vagrant.configure("2") do |config|
  # Configuración de cada nodo con IP específica

  # Nodo Manager
  config.vm.define "manager" do |manager|
    manager.vm.box = "ubuntu/bionic64"
    manager.vm.hostname = "manager"
    manager.vm.network "private_network", ip: "192.168.56.10"
    #manager.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "playbook.yml"
    #  ansible.extra_vars = {
    #    role: "manager"
    #  }
    #end
    manager.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 1
    end
  end

  # Sensores
  config.vm.define "sensor_movimiento" do |sensor_movimiento|
    sensor_movimiento.vm.box = "ubuntu/bionic64"
    sensor_movimiento.vm.hostname = "sensor-movimiento"
    sensor_movimiento.vm.network "private_network", ip: "192.168.56.21"
    #sensor_movimiento.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "playbook.yml"
    #  ansible.extra_vars = {
    #    role: "sensor",
    #    sensor_type: "movimiento"
    #  }
    #end
  end

  config.vm.define "sensor_luminoso" do |sensor_luminoso|
    sensor_luminoso.vm.box = "ubuntu/bionic64"
    sensor_luminoso.vm.hostname = "sensor-luminoso"
    sensor_luminoso.vm.network "private_network", ip: "192.168.56.22"
    #sensor_luminoso.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "playbook.yml"
    #  ansible.extra_vars = {
    #    role: "sensor",
    #    sensor_type: "luminoso"
    #  }
    #end
  end

  config.vm.define "sensor_temperatura" do |sensor_temperatura|
    sensor_temperatura.vm.box = "ubuntu/bionic64"
    sensor_temperatura.vm.hostname = "sensor-temperatura"
    sensor_temperatura.vm.network "private_network", ip: "192.168.56.23"
    #sensor_temperatura.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "playbook.yml"
    #  ansible.extra_vars = {
    #    role: "sensor",
    #    sensor_type: "temperatura"
    #  }
    #end
  end

  # Cámaras
  config.vm.define "camara_1" do |camara_1|
    camara_1.vm.box = "ubuntu/bionic64"
    camara_1.vm.hostname = "camara1"
    camara_1.vm.network "private_network", ip: "192.168.56.31"
    #camara_1.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "playbook.yml"
    #  ansible.extra_vars = {
    #    role: "camera",
    #    camera_name: "camara_1"
    #  }
    #end
  end

  config.vm.define "camara_2" do |camara_2|
    camara_2.vm.box = "ubuntu/bionic64"
    camara_2.vm.hostname = "camara2"
    camara_2.vm.network "private_network", ip: "192.168.56.32"
    #camara_2.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "playbook.yml"
    #  ansible.extra_vars = {
    #    role: "camera",
    #    camera_name: "camara_2"
    #  }
    #end
  end

  # Configuración general para todas las máquinas (excepto manager, que tiene memoria específica)
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "512"
    vb.cpus = 1
  end
end

