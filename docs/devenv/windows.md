# Windows Development Environment

1. Install VMWare Workstation
2. Setup Debian as Guest OS in VMWare
   Note: when prompted *Debian Software Selection*, untick "Desktop Environment".
3. Debian: set static IP address. For example: 

        iface eth0 inet static
            address 192.168.123.123
            gateway 192.168.123.2

4. Debian: install [dev-tool](toolset.md) especially vim, tmux, python.

5. Windows: Install [ConEmu][1]

6. Windows: Install [MinGW MSYS][2] or [Git Bash][3] (prefered)

7. Windows: Generate SSH key pair (public, private)

        ssh-keygen -t rsa

8. Debian: Add Windows public SSH key into Debian Authorized SSH Key
    `# File: ~/.ssh/authorized_keys`

9. Windows: Setup ConEmu to use MinGW MSYS bash shell

1. Windows - Bash Shell: Setup Alias to ssh to Debian

        # ~/.bashrc or ~/.bash_aliases
        alias devm="ssh <user>@<ip-address> -t tmux a

2. Windows: close VMWare Workstation window.
   When asked, choose run in background instead.

3. Windows: run ConEmu and use alias `devm` to connect to dev environment

[1]: http://conemu.github.io/
[2]: https://msysgit.github.io/
[3]: http://www.mingw.org/wiki/msys
