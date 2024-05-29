# ansible_laravel
Provisioning and deploying for your laravel project

## Create private public key 
Create your key under the ./key folder

```bash
ssh-keygen -t rsa -b 4096
```

## Config settings
Config all yours settings and variabile in group_vars/all.yml

## Provisioning web servers
Launch Ansible playbook to provisioning web servers

```bash
ansible-playbook -i inventory/development webservers_pb.yml
```

## Provisioning db servers
Launch Ansible playbook to provisioning db servers with sqlite/mysql

### Sqlite
```bash
ansible-playbook -i inventory/development sqlite_pb.yml
```

### Mysql
```bash
ansible-playbook -i inventory/development mysql_pb.yml
```

## Create your db on dbservers
Launch Ansible playbook to provisioning db servers with sqlite/mysql

### Sqlite
```bash
ansible-playbook -i inventory/development sqlite_create_db_pb.yml
```

### Mysql
```bash
ansible-playbook -i inventory/development mysql_create_db_pb.yml
```
