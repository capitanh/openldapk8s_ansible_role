Role Name
=========
This role installs openldap on kubernetes. Intended for development and tests purposes, not to be used as production server


Requirements
------------
None

Role Variables
--------------
This role requires the following variables to be defined elsewhere in the playbook that uses it. These are the default values:
```yaml
openldap_domain:            example.com
openldap_app_name:          openldap                      # helm chart release name
openldap_namespace:         openldap                      # k8s namespace
openldap_admin_password:    secret                        # admin user password
openldap_replicas:          1                             # k8s replicas count
openldap_nodeport:          30001                         # k8s Nodeport to access ldap server from outside cluster
```

Dependencies
------------
None

Example Playbook
----------------
Register the role in requirements.yml:
```yaml
- src: capitanh.openldapk8s-ansible-role
  name: openldap
```
Include it in your playbooks:
```yaml
- hosts: servers
  roles:
  - openldap
```

License
-------
BSD
