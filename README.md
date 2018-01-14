# Installation
Install the following:

 - python & pip

 - ansible

 - boto: pip install boto

# Requirements
  - Create a .boto in $HOME
```
#!python

    [Credentials]

    aws_access_key_id = <aws_key_id>

    aws_secret_access_key = <aws_secr>

```
- Create an AWS key_pair

# How to

Provision instance of type 'back' (instance configuration will be provided in a file located in ./ec2_vars/back.yml, see the default provided file app.yml):
``` shell
ansible-playbook -i localhost, -e "type=app" provision_ec2.yml
```

Resiliate :

!!!! Warning: As for now this may resiliate all instances !!! you will have to better target the instances to resiliate 

```shell
ansible-palaybook -i ec2.py terminate_ec2.yml

```
