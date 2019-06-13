## Introduction
This section is for deploying helm applications on  Kubernetes cluster.

### Prepare configuration and credentials
1. Create a credentials file in credentials directory. Use template file which is in template directiory. Update cluster_vars file according to your project and namespace names. If you have created a kubernetes cluster rather than "k8s-demo" create a directory with the name of the cluster in the configuration directory.

### Provisioning EKS cluster
1. Go to deploy-apps directory
2. Run the playbook to deploy helm applications.

```sh
ansible-playbook deploy-apps.yml -e "cluster_name=$cluster_name"
```
