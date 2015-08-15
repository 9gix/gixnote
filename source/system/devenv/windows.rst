.. _windows:

Windows Development Environment
===============================

#. Install VMWare Workstation
#. Setup Debian as Guest OS in VMWare
    Note: when prompted *Debian Software Selection*, untick "Desktop Environment".
#. Debian: set static IP address. For example: 
    .. code-block:: none

        iface eth0 inet static
            address 192.168.123.123
            gateway 192.168.123.2

#. Debian: install :ref:`dev-tool` especially vim, tmux, python.
#. Windows: Install `ConEmu`_
#. Windows: Install `MinGW MSYS`_ or `Git Bash`_ (prefered)
#. Windows: Generate SSH key pair (public, private)
    .. code-block:: bash

        ssh-keygen -t rsa

#. Debian: Add Windows public SSH key into Debian Authorized SSH Key
    ``# File: ~/.ssh/authorized_keys``
#. Windows: Setup `ConEmu`_ to use `MinGW MSYS`_ bash shell
#. Windows - Bash Shell: Setup Alias to ssh to Debian
    .. code-block:: bash

        # ~/.bashrc or ~/.bash_aliases
        alias devm="ssh <user>@<ip-address> -t tmux a

#. Windows: close VMWare Workstation window.
   When asked, choose run in background instead.
#. Windows: run `ConEmu`_ and use alias ``devm`` to connect to dev environment

.. _ConEmu: http://conemu.github.io/
.. _Git Bash: https://msysgit.github.io/
.. _MinGW MSYS: http://www.mingw.org/wiki/msys
