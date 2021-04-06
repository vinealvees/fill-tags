Role Name
=========

You can use this role to tag EC2 instance and EC2 volumes with the same tag

Requirements
------------

collections:
- amazon.aws
- community.aws

Role tested in Ansible 2.9.6, Python 3.8.5.

Role Variables
--------------
defaults/main.yml
```
AWSAccessKey: aws-access-key-here
AWSSecretAccessKey: aws-secret-access-key-here
AWSRegion: aws-regeion-here
ec2instanceid: aws-instance-id-here
```

Example Playbook
----------------

````
- name: Setting Tags on EC2 instances and volumes
  hosts: localhost
  connection: local
  environment:
    AWS_ACCESS_KEY_ID: '{{ AWSAccessKey }}'
    AWS_SECRET_ACCESS_KEY: '{{ AWSSecretAccessKey }}'
    AWS_DEFAULT_REGION: '{{ AWSRegion }}'
  roles:
    - fill-tags
````

License
-------

BSD

Author Information
------------------

Github: [vinealvees](https://github.com/vinealvees)
