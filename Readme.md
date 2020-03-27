# Ansible role for apache airflow

### Requirement

1. mysql server
    can use this role
    `git@gitlab.intra:kochi-infra-tools/mysql.git`

2. Database to be created
3. Mysql user to be provisioned
4. `explicit_defaults_for_timestamp: 1` to be added in my.cnf
5. DB credentials to be updated
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