$script = <<SCRIPT
apt update
apt install python-minimal -y
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.provision :shell, inline: $script

  config.vm.provision :ansible,
    playbook: 'playbook.yml',
    verbose: '-vv',
    sudo: true
end
