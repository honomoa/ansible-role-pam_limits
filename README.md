# Ansible Role: pam_limits

Modify Linux PAM limits.

[https://docs.ansible.com/ansible/2.6/modules/pam_limits_module.html](https://docs.ansible.com/ansible/2.6/modules/pam_limits_module.html)

# Role Variables

pam_limits: []

# Example Playbook

```
- hosts: server
  vars:
    pam_limits:
      - { domain: '*', type: 'soft', item: 'nofile', value: 1048576 }
      - { domain: '*', type: 'hard', item: 'nofile', value: 1048576 }
  roles:
    - { role: honomoa.pam_limits }
```

# License
CC BY-SA 3.0
