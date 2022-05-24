# Ansible role for apache airflow

### Requirement

1. Mysql server can use this role
    `git@github.com:Harijith-R/MySQL.git`

2. Database to be created
3. Mysql user to be provisioned
4. `explicit_defaults_for_timestamp: 1` to be added in my.cnf
5. DB credentials to be updated
6. SMTP details to be updated on airflow.cfg.j2
Update the airflow configuration parametes if required

### Sample Playbook

```yml
---
 - hosts: all
   become: yes
   roles:
    - mysql
    - apache-airflow
```