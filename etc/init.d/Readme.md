# sshd startup script for IRIX

1. Copy the `sshd` script in this directory to `/etc/init.d/`.

2. Create symlinks in runlevel control directories:

    - `sudo ln -s /etc/init.d/sshd /etc/rc0.d/K01sshd`
    - `sudo ln -s /etc/init.d/sshd /etc/rc2.d/S99sshd`

3. Create new chkconfig file `echo "on" > /var/config/sshd`

4. Start the service. Keys are generated automatically

    - `sudo /etc/init.d/sshd start`
