## Introduction
This section is for provisioning Kubernetes cluster on AWS-EKS.

### Prepare configuration and credentials
1. Update credentials in credentials directory and update cluster_vars in configuration directory. If you want to create a kubernetes cluster rather than "k8s-demo" create a directory with the desired name of the cluster in the configuration directory.

### Provisioning EKS cluster
1. Go to provision-clusters directory
2. Run the playbook to provision new cluster

```sh
ansible-playbook provision-cluster-eks.yml -e "cluster_name=$cluster_name"
```
