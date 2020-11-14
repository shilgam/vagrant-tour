# vagrant-tour

## Prerequisites

* [Vagrant](https://www.vagrantup.com/) installed

## Usage

1. clone this repo

1. cd into project's root dir

1. initialize a new Vagrant environment

        $ vagrant init

1. start the vagrant environment

        $ vagrant up

1. SSH into the machine
        $ vagrant ssh

1. interact with the machine and do whatever you want

1. stop the machine that Vagrant is managing and remove all the resources created

        $ vagrant destroy

1. remove the box

        # list your box files
        $ vagrant box list
        hashicorp/bionic64  (virtualbox, 1.0.282)

        # remove the box file
        $ vagrant box remove hashicorp/bionic64
