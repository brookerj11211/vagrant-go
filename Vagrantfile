Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provision :shell, inline: <<eos
set -x

VERSION=1.4
OS=linux
ARCH=amd64

profile='export PATH=$PATH:/usr/local/go/bin'

wget -q https://storage.googleapis.com/golang/go$VERSION.$OS-$ARCH.tar.gz
tar -C /usr/local -xzf go$VERSION.$OS-$ARCH.tar.gz
echo $profile > /etc/profile.d/gopath.sh

eos


end
