Ec2_cloudwatch_instance_recovery_alarm
=========

AWS EC2 cloudwatch auto recovery alarm in case of ec2 system health check fail , which means underlying hardware has some issues.

Additional information can be found here

```
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/UsingAlarmActions.html#AddingRecoverActions
```

Requirements
------------
#### Python Modules:

* boto
* boto3


Role Variables
--------------

* aws_profile: aws profile specified in ~/.aws/credentials file
* aws_region: aws region
* instance_name_tag: aws intance Name tag

Dependencies
------------

* ansible version: ansible 2.9.6


Example Playbook
----------------
```
---
- name: Playbook for AWS EC2 cloudwatch Auto recovery
  hosts: localhost
  connection: local
  gather_facts: False
  roles:
    - ec2_cloudwatch_instance_recovery_alarm

```

Example Playbook command lines
----------------

```
ansible-playbook playbook.yml -e aws_profile=default -e aws_region=us-east-1 -e instance_name_tag=APP

```

License
-------

BSD

Author Information
------------------

```
Sanket Raut
rautsankets@yahoo.com
linkedin.com/in/sanket-raut-49213017
```
