Vagrant Ansible utilizando VyOS y Ubuntu
==================================

Requirimientos
------------

**vagrant-vyos**

```
vagrant plugin install vagrant-vyos
```

**Python and poetry**

```
#sudo apt install python3 python3-pip python3-poetry
#pip3 install poetry
curl -sSL https://install.python-poetry.org | python3 - 
```

**Colecciones de Ansible**

```
poetry install
```

**Ansible vyos.vyos module**

```
poetry run ansible-galaxy collection install -r requirements.yml
```

Uso
-----

El laboratorio cuenta con dos carpetas en la cuales crea infraestructura de routers

**Infraestructura con rutas estaticas,no encrypta el tráfico**
* `cd site-to-site-static-route` para el directorio del laboratorio de vpns `vagrant up`
*  `vagrant ssh vyos1` o `vagrant ssh vyos2` contraseña vyos
*  `vagrant ssh ubuntu1` o `vagrant ssh ubuntu2` para entrar a los webserver

**Infraestructura con vpn, encrypta el tráfico**

* `cd site-to-site-ipsec-vpn` para el directorio del laboratorio de vpns `vagrant up`
* `vagrant ssh vyos1` o `vagrant ssh vyos2` contraseña vyos
*  `vagrant ssh ubuntu1` o `vagrant ssh ubuntu2` para entrar a los webserverss
* `cd site-to-site-static-route` para el directorio del laboratorio de vpns `vagrant up`

Tareas
------
1) Aprovisionar el lab rutas estaticas
2) Obtener la direccion ip del equipo ubuntu1, la cual generalmente es la 192.168.101.20
3) Conectarse a ubuntu2
4) lanzar el comando `hey -c 400 -n 30000 http://192.168.101.20`
5) Guardar la estadisticas
6) Destruir el laboratorio con `vagrant destroy -f`
7)  Aprovisionar el lab vpn
8) Obtener la direccion ip del equipo ubuntu1, la cual generalmente es la 192.168.101.20
9) Conectarse a ubuntu2
10) lanzar el comando `hey -c 400 -n 30000 http://192.168.101.20`