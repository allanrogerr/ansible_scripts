# ansible_scripts

# vm-broker
```
webservers:
  hosts:
    cluster0.lab.min.dev:
      ansible_host: 65.49.37.20
      ansible_port: 20456
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    cluster1.lab.min.dev:
      ansible_host: 65.49.37.20
      ansible_port: 20964
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    cluster2.lab.min.dev:
      ansible_host: 65.49.37.20
      ansible_port: 20880
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    cluster3.lab.min.dev:
      ansible_host: 65.49.37.20
      ansible_port: 20300
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
  vars:
    # General User variables
    user: ubuntu
    host_list: cluster0.lab.min.dev,cluster1.lab.min.dev,cluster2.lab.min.dev,cluster3.lab.min.dev
    minio_repo: https://github.com/allanrogerr/minio.git
    minio_branch: check-is-lxc
    host_prefix: cluster
    host_count: 4
    host_domain: lab.min.dev
    schema: https
```

```
ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i /home/ubuntu/vm-broker.yml -l webservers /home/ubuntu/ansible-scripts/ansible/main.yml
```