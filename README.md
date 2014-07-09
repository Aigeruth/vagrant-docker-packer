# Vagrant-Docker-Packer

Vagrant environment for building [Docker](https://www.docker.com/) images with
[Packer](http://www.packer.io/) on non-linux hosts (e.g. Mac OS X or
Windows).

You will have the following:

* Ubuntu 14.04
* Docker 1.1.0 (or newer, depends on the used [docker](https://supermarket.getchef.com/cookbooks/docker) cookbook version)
* Packer 0.6.0

## Requirements

* Vagrant 1.5 or newer and some plugins:
  * vagrant-berkshelf
  * vagrant-omnibus
* VirtualBox

You can install the required plugins like this:

```bash
vagrant plugin install vagrant-berkshelf
vagrant plugin install vagrant-omnibus
```

## Usage

Clone this repository and start the box:

```bash
git clone https://github.com/Aigeruth/vagrant-docker-packer.git
cd vagrant-docker-packer
vagrant up
vagrant ssh
cd /vagrant && packer build example/template.json
```
