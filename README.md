# ansible-dig2hosts

Provides an ansible playbook to do a dig zone transfer (AXFR) locally or via delegate.
Extracts the "A" DNS records and builds /etc/hosts flavored entries.
Adds entries to an Ansible managed block on the local /etc/hosts

## usage

```
ansible-playbook [--ask-become-pass] [-e delegate=delegate] -e domain=domain dig2hosts.yml
```

## example
```
ansible-playbook --ask-become-pass dig2hosts.yml -e delegate=vzjump2 -e domain=eng.vzwcorp.com
```
```
ansible-playbook --ask-become-pass dig2hosts.yml -e delegate=vzjump2 -e domain=hqplan.lab
```
