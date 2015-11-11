# Vagrant Magento

Vagrant box for running Magento on a private network.

## Pre-requisites

You will need Vagrant and Virtualbox installed.  If you do not have these you can install via Homebrew.

```sh
brew install caskroom/cask/brew-cask
brew cask install 'virtualbox'
brew cask install 'vagrant'
```

## Setup

- Copy `Vagrantfile` and `bootstrap.sh` to your project directory.

```sh
# /project/root

curl --remote-name https://raw.githubusercontent.com/kpheasey/vagrant_magento/master/Vagrantfile
curl --remote-name https://raw.githubusercontent.com/kpheasey/vagrant_magento/master/bootstrap.sh
```

- Place a copy of the Magento database dump in the same directory and name it `magento.sql`
- Update the `MAGENTO_ROOT` and `MAGENTO_TABLE_PREFIX` with appropriate values.
  - If Magento is in /public, then `MAGENTO_ROOT="/public"`
  - `MAGENTO_TABLE_PREFX` should include an underscore if necessary; `MAGENTO_TABLE_PREFIX="retail_"`
- Start vagrant; `vagrant up`
- Go to [http://192.168.50.50/](http://192.168.50.50/) in your browser

NOTE: If you don't already have the ubuntu/trusty64 box installed, it will be downloaded.  This is a big download, but it only happens once.

## Vagrant Manager

To place a convenient Vagrant management tool in the toolbar, you can install vagrant-manager via Homebrew.  This will allow you to control all of your Vagrant boxes in one place.

```sh
brew cask install 'vagrant-manager'
```
