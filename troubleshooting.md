# Error
The Node Source had an error:
Cannot load yaml data coming from Ansible: while scanning a simple key in 'string', line 2, column 1: -vvvv to see details ^ could not find expected ':' in 'string', line 3, column 1: all: ^
# Cause
The dash(-) in the group name in hosts.yml file.
```
all:
  vars:
    ansible_user: rundeck
  children:
    baxter-dev:
      hosts:
        baxter-dev:
          configfile: /etc/httpd/conf.d/baxter-dev.conf
    baxter-finance:
      hosts:
        baxter-fin:
          configfile: /etc/httpd/conf.d/baxter-fin.conf
```

# Solution
the error is caused by the dash(-) in group name, either remove it or replace it with underscore(_)
```
all:
  vars:
    ansible_user: rundeck
  children:
    baxter-dev:
      hosts:
        baxter_dev:
          configfile: /etc/httpd/conf.d/baxter-dev.conf
    baxter-finance:
      hosts:
        baxterfin:
          configfile: /etc/httpd/conf.d/baxter-fin.conf
```
