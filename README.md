# ansible_scripts

# vm-broker
```
webservers:
  hosts:
    source0.lab.min.dev:
      ansible_host: 65.49.37.22
      ansible_port: 20002
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    source1.lab.min.dev:
      ansible_host: 65.49.37.22
      ansible_port: 20012
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    source2.lab.min.dev:
      ansible_host: 65.49.37.22
      ansible_port: 20075
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    source3.lab.min.dev:
      ansible_host: 65.49.37.22
      ansible_port: 20013
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    source4.lab.min.dev:
      ansible_host: 65.49.37.22
      ansible_port: 20064
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    source5.lab.min.dev:
      ansible_host: 65.49.37.20
      ansible_port: 20029
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    source6.lab.min.dev:
      ansible_host: 65.49.37.20
      ansible_port: 20071
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    source7.lab.min.dev:
      ansible_host: 65.49.37.23
      ansible_port: 20070
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
  vars:
    # General User variables
    user: ubuntu
    host_list: source0.lab.min.dev,source1.lab.min.dev,source2.lab.min.dev,source3.lab.min.dev,source4.lab.min.dev,source5.lab.min.dev,source6.lab.min.dev,source7.lab.min.dev,source8.lab.min.dev
    minio_repo: https://github.com/allanrogerr/minio.git
    minio_branch: check-is-lxc_test
    host_prefix: source
    host_count: 8
    host_domain: lab.min.dev
    schema: https
```

```
ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i /home/ubuntu/vm-broker.yml -l webservers /home/ubuntu/ansible-scripts/ansible/main.yml
```