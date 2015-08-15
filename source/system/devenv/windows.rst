.. _windows:

Windows Development Environment
===============================

#. Install VMWare Workstation
#. Setup Debian as Guest OS in VMWare
   Note: when prompted *Debian Software Selection*, untick "Desktop Environment".
#. Debian: set static IP address
#. Debian: install :ref:`dev-tool` especially vim, tmux, python.
#. Windows: Install `ConEmu`_
#. Windows: Install `MinGW MSYS`_ or `Git Bash`_ (prefered)
#. Windows: Generate SSH key pair (public, private)
   ``ssh-keygen -t rsa``
#. Debian: Add Windows public SSH key into Debian Authorized SSH Key
   File: ``~/.ssh/authorized_keys``
#. Windows: Setup `ConEmu`_ to use `MinGW MSYS` bash shell
#. Windows - Bash Shell: Setup Alias to ssh to Debian
   ``alias debian="ssh <user>@<ip-address> -t tmux a``

.. _ConEmu: http://conemu.github.io/
.. _Git Bash: https://msysgit.github.io/
.. _MinGW MSYS: http://www.mingw.org/wiki/msys
