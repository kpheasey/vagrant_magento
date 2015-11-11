# Vagrant Magento

Vagrant box for running Magento on a private network.

## Pre-requisites

You will need Vagrant and Virtualbox installed.  If you do not have these you can install via homebrew.

```sh
brew install caskroom/cask/brew-cask
brew cask install 'virtualbox'
brew cask install 'vagrant'
```

## Setup

1. Copy `Vagrantfile` and `bootstrap.sh` to your project directory.
2. Place a copy of the Magento database dump in the same directory and name it `magento.sql`
3. Update the `MAGENTO_ROOT` and `MAGENTO_TABLE_PREFIX` with appropriate values.
  - If you Magento is in /public, then `MAGENTO_ROOT="/public"`
  - `MAGENTO_TABLE_PREFX` should include an underscore if necessary; `MAGENTO_TABLE_PREFIX="retail_"`
4. Start vagrant; `vagrant up`

NOTE: If you don't already have the ubuntu/trusty64 box installed, it will be downloaded.  This is a big download.

## Vagrant Manager

To place a convenient Vagrant management tool in the toolbar, you can install vagrant-manager via homebrew.  This will allow you to control all of your vagrant boxes in one place.

```sh
brew cask install 'vagrant-manager'
```
