# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = '2'
Vagrant.configure(VAGRANTFILE_API_VERSION) do|config|
  config.ssh.insert_key = false
  config.vm.provider :virtualbox do|vb|
    vb.customize ['modifyvm', :id, '--memory', '2048']
  end

  #Web Server
  config.vm.define 'master' do|web|
    web.vm.hostname = 'master'
    web.vm.box = 'bento/ubuntu-22.04'
    web.vm.network 'private_network', ip: '192.168.56.157'
  end

  #Web Server
  config.vm.define 'node1' do|web|
    web.vm.hostname = 'node1'
    web.vm.box = 'bento/ubuntu-22.04'
    web.vm.network 'private_network', ip: '192.168.56.158'
  end

  #Web Server
  config.vm.define 'node2' do|web|
    web.vm.hostname = 'node2'
    web.vm.box = 'bento/ubuntu-22.04'
    web.vm.network 'private_network', ip: '192.168.56.159'
  end

end