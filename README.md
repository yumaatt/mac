# how to use

## git clone setting repository

```
git clone https://github.com/yumaatt/mac.git ~/.ghq/github.com/yumaatt/mac
~/.ghq/github.com/yumaatt/mac/setup.sh
```

## install xcode

```
sudo xcodebuild -license
xcode-select --install
```

## install homebrew

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update
```

## install ansible

```
brew install ansible
git clone https://github.com/yumaatt/ansible-playbooks.git ~/.ghq/github.com/yumaatt/ansible-playbooks
cd ~/.ghq/github.com/yumaatt/ansible-playbooks/yumaatt
touch private_vars/admin{,-development,-development-mac}.yml
ansible-playbook site.yml -i hosts -l admin-development-mac -K -C
ansible-playbook site.yml -i hosts -l admin-development-mac -K
```

## install other softwares

by gui

## install vagrant

```
mkdir ~/vagrant/ubuntu14_development
ln -s ~/.ghq/github.com/yumaatt/mac/vagrant/ubuntu14_development/Vagrantfile ~/vagrant/ubuntu14_development/
cd ~/vagrant/ubuntu14_development/
vagrant box add ubuntu14_dev1 https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box
vagrant init ubuntu14_dev1
vagrant up
vagrant ssh dev1

vagrant plugin install sahara
vagrant sandbox on && vagrant ssh dev1
vagrant sandbox rollback && vagrant sandbox off
vagrant sandbox commit && vagrant sandbox off
```
