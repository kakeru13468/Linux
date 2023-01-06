# linux note
- `ifconfig` -->check head is 10 ip address
- `tail -f /var/log/secure`
    - open Windows powershell
    - `ssh e901@Ip_address`
        - you should  enter your password
        - try success
        - try fail
    - check terminal message

# firewall
**test important**
- `systemctl status firewall` (open firewall)
- `systemctl stop firewall` (close firewall)
    - `systemctl enable firewall` (if you want firewall always open, you can use this command)
- `systemctl status httpd` (check http)
- `systemctl start httpd` (run http)
- `systemctl status httpd`
    - `cd /var/www/html`
    - `echo "number A9235689" > index.html`
    - go to your browser and input your ipaddress

# package
**11.2.2**
- `cd /dev/shm`
- `tar -cvf etc.tar /etc` (package)
- `ll` (check package)

**11.2.3**
- `vim test`
    - `#!/bin/bash`
    - `source='/etc /home' `
    - `target="bak_sys_$(date +%Y_%m_%d).tar"`
    - `tar -cvf $target $source`

**11.3.2**
- `crontab -e`
    - `*/1 * * * * date >> /tmp/test.log`
- `tail -f /tmp/test.log` 