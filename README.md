Vagrant Ansible examples with VyOS
==================================

Requirements
------------

* vagrant-vyos

```
vagrant plugin install vagrant-vyos
```

* Python and poetry

```
sudo apt install python3 python3-pip python3-poetry
pip3 install poetry
```

* Ansible

```
poetry install
```

* Ansible vyos.vyos module

```
poetry run ansible-galaxy collection install -r requirements.yml
```

Usage
-----

* `cd site-to-site-ipsec-vpn` para el directorio del laboratorio de vpns `vagrant up`
* `cd site-to-site-static-route` para el directorio del laboratorio de vpns `vagrant up`