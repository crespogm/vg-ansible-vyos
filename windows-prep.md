Vagrant Ansible examples with VyOS
==================================
Instalation
* vagrant
* choco
* WSL2 with Ubuntu 20.04 image
* Ansible
* VirtualBox

Choco
------------
Abrir un cmd como ADMINISTRADOR y lanzar el comando
´´´
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "[System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
´´´
Virtualbox
------------
choco install virtualbox
apretar la letra A cuando pregunte por los scripts.
En caso de que te de error, y solicite reinicio, reiniciar el equipo y 

Vagrant
------------
choco install vagrant
