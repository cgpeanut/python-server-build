# python-server
- Install devtools 
- yum groupinstall -y "Development Tools"
- yum install -y zlib-devel

- Install python 3.7.3 from source 
- wget https://python.org/ftp/python/3.7.3/Python-3.7.3.tar.xz
- tar xf Python-3.7.3.tar.xz 
- cd Python-3.7.3

- ./configure --enable-optimizations --with-ensurepip=install
- make altinstall  
- sudo /usr/local/bin/pip3.7 install --upgrade pip

- sudo cat /etc/sudoers | grep secure_path
- add /usr/local/bin
