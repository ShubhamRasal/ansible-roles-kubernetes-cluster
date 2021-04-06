provisionEC2
=========

This role is used to launch EC2 instances on AWS. 

Requirements
------------

boto library.

Role Variables
--------------

- accessKey: Set AWS_ACCESS_KEY value here. 
- secretKey: Set AWS_SECRET_KEY value here. 
- OS_Names: This is like of OS we want to launch on top of AWS.
*       Ex: OS_Names: 
              - k8s_master
              - k8s_slave1
              - k8s_slav2
- Also, you can include VPC, SubnetID, AMI, counts accordingly in vars file. But, here to simplicity, I have made it fixed to default configuration on AWS. 

Example Playbook
----------------

    - hosts: localhost
      roles:
         - /root/k8s_play/role/provisionEC2 (complete path of role)

