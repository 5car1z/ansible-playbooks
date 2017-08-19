# Local Testing with Vagrant

Tested with Vagrant 1.9.4

This provides easy test deployment to a local Vagrant virtual machine. 

The configuration file uses a [Debian 8 (Jessie) box](https://app.vagrantup.com/debian/boxes/jessie64) for the VM test environment. 

To get a machine up, run:

```bash
$ vagrant up
```

This will give you a virtual machine with a complete base server environment
at IP address `192.168.111.223`.

If you want to re-play the Ansible playbook, run:

```bash
$ vagrant provision
```

Running Ansible manually can be done like this:

```bash 
$ ansible-playbook -i inventory.yml ../playbook.yml
```

See the Vagrant section for more details at: http://www.tricksofthetrades.net/2017/08/21/ansible-playbook-server-provisioning/
