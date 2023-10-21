# ansible_scripts

# vm-broker
```
webservers:
  hosts:
    cluster0.lab.min.dev:
      ansible_host: 65.49.37.21
      ansible_port: 20042
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    cluster1.lab.min.dev:
      ansible_host: 65.49.37.21
      ansible_port: 20093
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    cluster2.lab.min.dev:
      ansible_host: 65.49.37.23
      ansible_port: 20074
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    cluster3.lab.min.dev:
      ansible_host: 65.49.37.22
      ansible_port: 20022
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    cluster4.lab.min.dev:
      ansible_host: 65.49.37.22
      ansible_port: 20017
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    cluster5.lab.min.dev:
      ansible_host: 65.49.37.22
      ansible_port: 20076
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    cluster6.lab.min.dev:
      ansible_host: 65.49.37.22
      ansible_port: 20084
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
    cluster7.lab.min.dev:
      ansible_host: 65.49.37.22
      ansible_port: 20019
      ansible_connection: ssh
      ansible_user: ubuntu
      ansible_ssh_user: ubuntu
      ansible_ssh_private_key_file: /home/ubuntu/.ssh/id_ecdsa
  vars:
    # General User variables
    user: ubuntu
    host_list: cluster0.lab.min.dev,cluster1.lab.min.dev,cluster2.lab.min.dev,cluster3.lab.min.dev,cluster4.lab.min.dev,cluster5.lab.min.dev,cluster6.lab.min.dev,cluster7.lab.min.dev
    minio_repo: https://github.com/allanrogerr/minio.git
    minio_branch: cluster-lxc-containers
    host_prefix: cluster
    host_count: 8
    host_domain: lab.min.dev
    schema: https
```

```
ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i /home/ubuntu/vm-broker.yml -l webservers /home/ubuntu/ansible-scripts/ansible/main.yml
```