# Bandit Level 26 → Level 27

## Objetivo

Hay un repositorio de git en `ssh://bandit27-git@localhost/home/bandit27-git/repo`. La contraseña para el usuario `bandit27-git`es la misma que para el usuario `bandit27`.

Clona el repositorio y encuentra la contraseña para el siguiente nivel.
## Datos de acceso al nivel
- bandit27 
- YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
## Solucion
```
bandit27@bandit:/tmp/tmp.RH39ki24pd$ git clone ssh://bandit27-
git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)'
can't be established.
ED25519 key fingerprint is
SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting
(yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission
denied).
Failed to add the host to the list of known hosts
(/home/bandit27/.ssh/known_hosts).
_ _ _ _
| |__ __ _ _ __ __| (_) |_
| '_ \ / _` | '_ \ / _` | | __|
| |_) | (_| | | | | (_| | | |_
|_.__/ \__,_|_| |_|\__,_|_|\__|
This is an OverTheWire game server. 

More information on http://www.overthewire.org/wargames
bandit27-git@localhost's password: YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
bandit27@bandit:/tmp/tmp.RH39ki24pd$ ls -la
total 76
drwx------ 3 bandit27 bandit27 4096 Feb 28 12:56 .
drwxrwx-wt 1742 root root 69632 Feb 28 12:56 ..
drwxrwxr-x 3 bandit27 bandit27 4096 Feb28 12:56 repo
bandit27@bandit:/tmp/tmp.RH39ki24pd$ cd repo/
bandit27@bandit:/tmp/tmp.RH39ki24pd/repo$ ls
README
bandit27@bandit:/tmp/tmp.RH39ki24pd/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19n
```

## Notas adicionales
El archivo **README** a menudo se encuentra en un repositorio de git. Se usa como una descripción general de todos los archivos en un directorio o el proyecto git. Al crear un proyecto git, un archivo README es útil para recordar de qué se trata el proyecto, así como otra información que los usuarios y desarrolladores puedan necesitar. Por ejemplo, una breve explicación del proyecto, instrucciones de configuración e instalación, información de licencias y más.
## Referencias
- https://mayadevbe.me/posts/overthewire/bandit/level28/