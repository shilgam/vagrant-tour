# vagrant-tour

## Prerequisites

* [Vagrant](https://www.vagrantup.com/) installed

## Usage

1. clone this repo

1. cd into project's root dir

1. setup VM environment

    1. initialize a new Vagrant environment

            $ vagrant init

    1. start the vagrant environment

            $ vagrant up

1. interact with the VM environment

    1. load http://127.0.0.1:4567 in your browser where you will find a web page that is being served from the guest virtual machine.

    1. SSH into the machine

            $ vagrant ssh

            # test the synced folder
            vagrant@vagrant:~$ ls /vagrant/foo

1. teardown VM environment

    1. suspend the machine

            $ vagrant suspend

        NOTE: it is intended for stopping and starting work quickly. The downside is that the virtual machine will still use disk space while suspended, and requires additional disk space to store the state of the virtual machine RAM.

    1. halt the machine

            $ vagrant halt

        Halting the virtual machine will gracefully shut down the guest operating system and power down the guest machine.
        NOTE: A halted guest machine will take more time to start from a cold boot and will still consume disk space.

    1. destroy the machine

            $ vagrant destroy

        It will remove all traces of the guest machine from your system, stop the guest machine, power it down, and reclaim its disk space and RAM.

    1. remove the box

            # list your box files
            $ vagrant box list
            hashicorp/bionic64  (virtualbox, 1.0.282)

            # remove the box file
            $ vagrant box remove hashicorp/bionic64
