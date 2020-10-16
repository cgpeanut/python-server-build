# python-server setup
...
Install devtools 
yum groupinstall -y "Development Tools"
yum install -y zlib-devel

# Install python 3.7.3 from source 

- $ wget https://python.org/ftp/python/3.7.3/Python-3.7.3.tar.xz
- $ tar xf Python-3.7.3.tar.xz 
- $ cd Python-3.7.3
- $ ./configure --enable-optimizations --with-ensurepip=install
- $ make altinstall  
- $ sudo /usr/local/bin/pip3.7 install --upgrade pip
- $ sudo cat /etc/sudoers | grep secure_path
- $ add /usr/local/bin

# setup VS Code for Remote SSH to cloud VM

$ install VS code software 
# here are the 3 VS code extensions

$ remote development extension
$ python
$ pyright
$ Settings Sync
$ Vim

# pipenv crash course 
# set ssh
$ ssh-keygen -t rsa -b 4096 -C "robertoruizroxas@gmail.com" -f ~/.ssh/id_rsa-remote-ssh
$ ssh-copy-id -i ~/.ssh/id_rsa-remote-ssh.pub cloud_user@robertoruizroxas.mylabserver.com

# setup vs code .ssh/osconfig 
- Host python3-cloud
  - User cloud_user
  - HostName 7938ac48b61c.mylabserver.com
  - IdentityFile "C:\Users\audiophile\.ssh\id_rsa-remote-ssh"
  - LocalForward 127.0.0.1:8080 127.0.0.1:8080
- add to .ssh/config (local)
- Host python3-cloud
  - User cloud_user
  - HostName 7938ac48b61c.mylabserver.com
  - IdentityFile "C:\Users\audiophile\.ssh\id_rsa-remote-ssh"
  - LocalForward 127.0.0.1:8080 127.0.0.1:8080
- Host python-server
  - User rroxas
  - HostName python-server
  - IdentityFile "C:\Users\audiophile\.ssh\id_rsa-remote-ssh

# modularized python setup basics
- create main and module directory in vs code
  - mkdir -p assault/assault 
  - inside assault create README.md (describe your module)
  - 

# developement 
- for working on assault, you'll need to have Python >=3.7 (because 'asyncio') and ['pipenv']
- $ pipenv install --dev
- $ pipenv shell (activate shell)

# download setup.py and .gitignore
- $ cd assault
- $ curl -O https://github.com/cgpeanut/python-server-build/blob/main/assault/setup.py
- $ curl -O https://github.com/navdeep-G/setup.py/blob/master/setup.py (untouched)
- $ cure -o https://github.com/github/gitignore/blob/master/Python.gitignore

