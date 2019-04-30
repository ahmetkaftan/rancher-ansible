## Introduction
This section is for provisioning an ec2 instance on AWS and deploying single node Rancher.

### Steps to be done before once for all:
1. Create a file named "credentials" file in credentials directory. Use template/credentials/credentials.tmpl file as template.

### Create configuration file
1. Run the playbook to create an ec2 instance and deploy rancher.

```sh
ansible-playbook provision-rancher.yml
```

### Upgrade/downgrade Rancher container image version
1. Update rancher_tag variable in rancher_vars file.
2. Run the following command:
```sh
ansible-playbook upgrade-rancher.yml
```