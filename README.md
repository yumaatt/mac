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
cd ~/.ghq/github.com/yumaatt/mac/ansible-playbooks
ansible-playbook -i local site.yml -K --check
ansible-playbook -i local site.yml -K
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
