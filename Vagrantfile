Vagrant.configure("2") do |config|  
  config.vm.box = "pmonteiro/manjaro-21-X64-gnome"
  config.vm.box_version = "1.0.0"
    config.vm.provider "virtualbox" do |vb|
    vb.name = "manjaro-gnome"
    vb.customize ["modifyvm", :id, "--usb", "off"]
    vb.customize ["modifyvm", :id, "--usbehci", "off"]
  end
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
