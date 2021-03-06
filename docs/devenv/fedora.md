# Setup Fedora as Development Environment

```bash
    # Kernel headers, compiler, etc
    yum install kernel-headers kernel-devel gcc

    # Yakuake is very useful if you use multiple terminal or screen
    sudo yum install yakuake

    # Autostart Yakuake
    sudo cp /usr/share/applications/kde4/yakuake.desktop /etc/xdg/autostart/

    # Source Code Management
    sudo yum install git hg svn

    # Best Text Editor
    sudo yum install vim

    # Python Package manager
    sudo yum install python-pip

    # Python VirtualEnv
    sudo pip-python install virtualenvwrapper
    mkdir ~/.virtualenvs
```

Copy this into `~/.bashrc` file

```bash
    export WORKON_HOME=$HOME/.virtualenvs
    export PROJECT_HOME=$HOME/Workspace
    source /usr/local/bin/virtualenvwrapper.sh
```

[Install Eclipse](http://www.if-not-true-then-false.com/2010/linux-install-eclipse-on-fedora-centos-red-hat-rhel/)

```bash
    mkdir ~/.ssh
    cp aws-server.pem ~/.ssh
```

Create script to ssh production & staging server on your home directory


```bash
    ssh -t -i ~/.ssh/aws-server.pem ec2-user@ip-address screen -R YourName
```


```bash
    # Create and Copy the Key into Github Key Management 
    ssh-keygen
    cat ~/.ssh/id_rsa.pub
```

Clone project

```bash
    git clone git@github.com:Account/project.git
```

Setup GitConfig File
[Alias](git-alias.md)

```
    [user]
        name = YourName
        email = email@email.com
```

Make Virtual Environment


```bash
    mkvirtualenv project --distribute
    workon project
```

Setup Project


```bash
    # Setup Necessary Python Library
    sudo yum install python python-devel

    # Setup MySQL if necessary
    sudo yum install mysql mysql-server mysql-devel

    # If you need PIL library
    sudo yum install python-imaging

    # Install Requirement
    pip install -r requirements.txt
```


[Install NodeJS](http://nodejs.tchol.org/)

This is to allow Sudo user to run execute node.

```bash
    sudo ln -s /usr/local/bin/node /usr/bin/node
    sudo ln -s /usr/local/lib/node /usr/lib/node
    sudo ln -s /usr/local/bin/npm /usr/bin/npm
    sudo ln -s /usr/local/bin/node-waf /usr/bin/node-waf
```

Setup Memcached

```bash
    yum install memcached libmemcached libmemcached-devel
    pip install pylibmc python-memcached
```
    
Setup PostgreSQL with PostGIS

```bash
    yum install postgresql-server
    yum install postgresql
    yum install postgis

    postgresql-setup initdb
    service postgresql start
    chkconfig postgresql on

    sudo -u postgres psql
    > create user eugene createdb createuser password 'password';

    createdb eugene

    # For POSTGIS
    psql
    > CREATE EXTENSION postgis;
    > CREATE EXTENSION postgis_topology;
```

PostGIS setup troubleshoot: 

* [PostGIS Yum Installation][1]
* [PostGIS User Permission][2]
* [PostGIS Django Troubleshoot][3]

Extras:

```bash
    sudo rpm -Uvh http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-stable.noarch.rpm
```

I hope I didn't miss any step. If I do I'll update this post.


[1]: http://wiki.postgresql.org/wiki/YUM_Installation
[2]: http://www.postgresql.org/message-id/4D958A35.8030501@hogranch.com
[3]: https://docs.djangoproject.com/en/dev/ref/contrib/gis/install/#troubleshooting
