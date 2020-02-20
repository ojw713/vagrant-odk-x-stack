# ODK-X Stack in a Box

This repository will install the [ODK-X](https://opendatakit.org/software/odk-x/) (Sync Endpoint)


## Vagrant and Ansible

**This repositiory requires the [vagrant reload plugin](https://github.com/aidanns/vagrant-reload)**
- `vagrant plugin install vagrant-reload`

Do a simple `vagrant up` by using [Vagrant](https://www.vagrantup.com)'s [Ansible provisioner](https://www.vagrantup.com/docs/provisioning/ansible.html). All you need is a working [Vagrant installation](https://www.vagrantup.com/docs/installation/) (2.2.4+ but the latest version is always recommended), a [provider](https://www.vagrantup.com/docs/providers/) (tested with the latest [VirtualBox](https://www.virtualbox.org) version), and 3GB of RAM.

If more than the default 10GB disk space is needed
- run `vagrant plugin install vagrant-disksize` to install the vagrant plugin
- add `ubuntu.disksize.size = "25GB"` to the Vagrantfile.


## Future Plans

- Setup more ODK tools (ODK-X Application Designer and Suitcase)
- Separate Configurations for DB, LDAP, etc.


## ODK Web-UI

Access at [http://127.0.0.1:8081/web-ui/login](http://127.0.0.1:8081/web-ui/login).

Default ODK users

Site Admin:
- username: `syncadmin`

Sync User:
- username: `syncuser`

The passwords are defined in the [vars.yml](https://raw.githubusercontent.com/ojw713/vagrant-odk-x-stack/master/odk-x-stack/vars.yml) file.


## ODK LDAP Admin

Access at [https://127.0.0.1:40000](https://127.0.0.1:40000).

See ODK Sync setup [documenation](https://docs.opendatakit.org/odk-x/sync-endpoint-setup/#sync-endpoint-setup-create-user) for LDAP Admin credentials.


## ODK Postgres DB Connection

Access at [http://127.0.0.1:5432](http://127.0.0.1:5432).

Default credentials are containted in the `sync-endpoint-default-setup` [db.env](https://raw.githubusercontent.com/opendatakit/sync-endpoint-default-setup/master/db.env)

