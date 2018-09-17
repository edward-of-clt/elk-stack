# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    vb.memory = 1024
  end

  config.vm.define "elastic1" do |elastic|
    elastic.vm.box = "centos/7"
    elastic.vm.network "private_network", ip: "192.168.33.2"
    elastic.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/vagrant.yml"
    end
  end

  config.vm.define "elastic2" do |elastic|
    elastic.vm.box = "centos/7"
    elastic.vm.network "private_network", ip: "192.168.33.12"
    elastic.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/vagrant.yml"
    end
  end

  config.vm.define "elastic3" do |elastic|
    elastic.vm.box = "centos/7"
    elastic.vm.network "private_network", ip: "192.168.33.22"
    elastic.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/vagrant.yml"
    end
  end

  config.vm.define "logstash" do |logstash|
    logstash.vm.box = "centos/7"
    logstash.vm.network "private_network", ip: "192.168.33.3"
    logstash.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/vagrant.yml"
    end
  end

  config.vm.define "kibana" do |kibana|
    kibana.vm.box = "centos/7"
    kibana.vm.network "private_network", ip: "192.168.33.4"
    kibana.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/vagrant.yml"
    end
  end

  config.vm.define "kibana2" do |kibana|
    kibana.vm.box = "centos/7"
    kibana.vm.network "private_network", ip: "192.168.33.14"
    kibana.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/vagrant.yml"
    end
  end

  config.vm.define "queue" do |queue|
    queue.vm.box = "centos/7"
    queue.vm.network "private_network", ip: "192.168.33.5"
    queue.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/vagrant.yml"
    end
  end

  config.vm.define "webserver" do |webserver|
    webserver.vm.box = "centos/7"
    webserver.vm.network "private_network", ip: "192.168.33.6"
    webserver.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/vagrant.yml"
    end
  end
end
