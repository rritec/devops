======================
SSH Passwordless Login 
======================
1. Create three instances of ec2 machines

2. Name master,dev and prod respectively

**Master Server**

3. In master server ``sudo -i`` > ``ssh-keygen`` > press enters

4. Navigate to ls ~/.ssh/

5. Observe two files created ``id_rsa`` and ``id_rsa.pub``

6. cat ~/.ssh/id_rsa.pub 

7. Copy the key from ``id_rsa.pub`` 

**Client Servers**

1. paste into other server ``vi ~/.ssh/authorized_keys``

2. vi /etc/ssh/sshd_config 

3. make ``passwordauthentication no`` to ``passwordauthentication
yes``

4. In master server ``ssh <ip>``> ``yes`` and observe it will login without asking password

================
Install Ansible
================

1. In master server ``amazon-linux-extras install ansible2``

2. ``ls /etc/ansible`` observe all files

3.  vi /etc/ansible/hosts

4. Add a group and add private ips of client servers

    [dev]

    172.31.32.154

    172.31.33.85

5.  ``ansible -m ping all``


