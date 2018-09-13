# etcd3cluster-ansible



A ansible script to installs etcd 3.x cluster on CentOS 7

## Features
* etcd cluster with ca/tls support
* time sync source configured
* firewall port rules configured 


## Requirements

* ansible 2.4


## Example

1. enter script directory, modify inventories settings (in ./inventories/dev/, node name and ip address of etcd cluster  );

   default cluster setting:
      [etcd-nodes]
      node1
      node2
      node3

   ip address of nodes:
      node1 - 192.168.100.101
      node2 - 192.168.100.102
      node3 - 192.168.100.103

2. modify proxy setting in ./deploy-etcd3.yml

and enter script directory, then, 

```
ansible-playbook -i inventories/dev/hosts deploy-etcd3.yml
```

rem: check ./tmp directory for a backup of files to generate certs and ca/cert files generated. 

check how-to.txt for detailed intro
