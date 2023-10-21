# ansible_scripts

# vm-broker
webservers:
    hosts:
        cluster0.lab.min.dev:
            ansible_host: 65.49.37.23
            ansible_port: 30010
            ansible_user: ubuntu
            ansible_connection: ssh
            ansible_ssh_user: ubuntu
            ansible_ssh_private_key_file: old
    vars:
        # General User variables
        host_list: cluster0.lab.min.dev,cluster1.lab.min.dev,cluster2.lab.min.dev,cluster3.lab.min.dev,cluster4.lab.min.dev,cluster5.lab.min.dev,cluster6.lab.min.dev,cluster7.lab.min.dev,
        minio_repo: https://github.com/allanrogerr/minio.git
        minio_branch: cluster-lxc-containers
        host_prefix: cluster
        host_count: 8
        host_domain: lab.min.dev
        schema: https