k8s_master
=========

This role is used to configure Master node of kubernetes cluster. 


Dependencies
------------

This role is dependent on **provisionEC2** role. This role fetches the hosts dynamically using dynamic inventory. So, it is necessary to launch instances first and then this role to be run so that dynamic inventory can fetch the IP and configure accordingly. So, here the main concept of tagging the instance come in play. So, we can ping a particular host using it's tag name. For ex: If a OS has tag "k8s_Master", then its host will be **"tag_Name_k8s_Master"**. So, calling this role, we can put the hosts as ["tag_Name_k8s_Master"].

Example Playbook
----------------

    - hosts: ["tag_Name_k8s_Master"]
      roles:
         - /root/k8s_play/role/k8s_Master (complete path of the role)


