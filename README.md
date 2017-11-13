
# VerosK.nginx

This is Ansible role which sets-up proftpd with 
FTP virtual users.

```yaml

  hosts: ftp
  vars:
    proftpd_with_tls: False

    proftpd_default_user: backup
    proftpd_default_user_password: changeme
    proftpd_default_user_uid: 1002
    proftpd_default_user_gid: 1002
    proftpd_default_user_gecos: "Backup user"
    proftpd_default_user_homedir: "/backup/"

  roles:
    - role: geerlingguy.repo-epel
    - role: VerosK.proftpd
```

# License

2-BSD