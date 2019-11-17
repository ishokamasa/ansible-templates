Ansible-template
===

Ansible template for CentOS7 later not support Any other os.
Please setup local Mac to use this template.


## Setup
### Local Mac Hosts

Add ssh configuration to local mac hosts file to you could be ssh ssh password.

```sh
# sudo vim ~/.ssh/config
Host SSH_TAB_COMPLEMENT_NAME
  HostName IPADDRESS or Set Hostname could be resolve name over internet
  User root
  #IdentityFile ~/.ssh/id_rsa_2017
```

### Ansible Hosts

Create hosts file into this repository.
```sh
$ vim hosts
[app]
HOSTNAME <- set hostname wrote in .ssh/config
```

## Deploy

Dryrun
```sh
ansible-playbook -i hosts main.yml -t base -Dk -C
```

Apply
```sh
ansible-playbook -i hosts main.yml -t base -Dk
```
