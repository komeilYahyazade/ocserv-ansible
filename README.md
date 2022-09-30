OCserv Ansible
=========

Requirements
------------

+ An internal ubuntu server (located in your country)
+ An external ubuntu server (located abroad)
+ Ansible installed on your local

How To Use
----------------
first, resolve your domain to external server ip

then, open ./haproxy/vars/main.yml and according to given example update 

vpn_hosts variable.

Then, just simply run command below:

```bash
ansible-playbook -i inventory.ini --become ocserv.yml
 ```

At last, if all tasks done successfully, resolve your domain to internal
server ip.


Also we put a bash script on vpn servers (not haproxy servers) for creating new users.

Example:

```
ocuser username
```

Output:
```
username: username
password: random_password
host: vpn.domain.com
```
