# vagrant-learn


### Installation 


```bash
export VAGRANT_VERSOIN="2.2.5"

wget https://releases.hashicorp.com/vagrant/${VAGRANT_VERSION}/vagrant_${VAGRANT_VERSION}_linux_amd64.zip
gunzip -c ./vagrant_${VAGRANT_VERSION}_linux_amd64.zip > ./vagrant

rm ./vagrant_${VAGRANT_VERSION}_linux_amd64.zip
chmod +x vagrant
mv ./vagrant /usr/bin/vagrant

# only linux, kvm, virtualbox
[[ $(lsmod | grep kvm_intel) ]] && { 
  echo 'blacklist kvm-intel' >> /etc/modprobe.d/blacklist.conf
}
 echo  "export VAGRANT_DISABLE_VBOXSYMLINKCREATE=1" >> $HOME/.profile
 export VAGRANT_DISABLE_VBOXSYMLINKCREATE=1

```

more info [linux, kvm, virtualbox](https://www.vagrantup.com/docs/installation/#linux-virtualbox-and-kvm)



### get a box


```bash
$ vagrant install 
