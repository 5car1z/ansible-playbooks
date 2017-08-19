Local deployment with Vagrant
=============================

Tested with Vagrant 1.7.2.

This provides easy deployment on a local virtual machine using Vagrant. The
configuration is based on a
[Debian 8 (Jessie) box](https://git.lumc.nl/m.vermaat.hg/vagrant-debian-jessie-64).

To get a machine up, run:

    vagrant up

This will give you a virtual machine with a complete base server environment
at IP address `192.168.111.223`.

If you just want to re-play the Ansible playbook, run:

    vagrant provision

Running Ansible manually can be done like this:

    ANSIBLE_HOST_KEY_CHECKING=False \
      ansible-playbook -i inventory.yml ../playbook.yml

(Unfortunately, there seems to be no easier way to disable host key checking
for the Vagrant host only.)

You can SSH into the machine with:

    vagrant ssh
