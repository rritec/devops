======================
SSH Passwordless Login 
======================
1. Create three instances of ec2 machines

2. Name master,dev and prod respectively

3. In master server ``sudo -i`` > ``ssh-keygen`` > press enters

4. Observe two files created ``id_rsa`` and ``id_rsa.pub``

5. copy the key from ``id_rsa.pub`` and paste into other server ``.ssh/authorized_keys``

6. In master server ``ssh <user>@<ip>`` and observe it will login without asking password

================
Install Ansible
================

1. In master server ``amazon-linux-extras install ansible2``
