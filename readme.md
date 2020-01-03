# ODK-X Stack in a Box

This repository will install the [ODK-X](https://opendatakit.org/software/odk-x/) (ODK-X Tables, Survey, Services, Application Designer, Suitcase, Sync Endpoint)


## Vagrant and Ansible

Do a simple `vagrant up` by using [Vagrant](https://www.vagrantup.com)'s [Ansible provisioner](https://www.vagrantup.com/docs/provisioning/ansible.html). All you need is a working [Vagrant installation](https://www.vagrantup.com/docs/installation/) (2.2.4+ but the latest version is always recommended), a [provider](https://www.vagrantup.com/docs/providers/) (tested with the latest [VirtualBox](https://www.virtualbox.org) version), and 3GB of RAM.

If you want more modify the 10GB disk space, run `vagrant plugin install vagrant-disksize` to install the plugin.

With the [Ansible playbooks](https://docs.ansible.com/ansible/playbooks.html) in the */odk-x-stack/* folder you can configure the whole system step by step (TBD.)

Future Plans

- Add users and groups to LDAP via command line
- Setup more ODK tools (ODK-X Application Designer and Suitcase)
- Separate Configurations for DB, LDAP, etc.


## ODK Web-UI

Access Kibana at [http://127.0.0.1:8081](http://127.0.0.1:8081).


## ODK LDAP Admin

Filebeat port for Logstash at [https://127.0.0.1:40000](https://127.0.0.1:40000).
