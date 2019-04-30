## Introduction
This section is for provisioning an ec2 instance on AWS and deploying single node Rancher.

### Steps to be done before once for all:
1. Create a file named "credentials" file in credentials directory. Use template/credentials/credentials.tmpl file as template.

### Create configuration file
1. Run the playbook to create an ec2 instance and deploy rancher.

```sh
ansible-playbook provision-rancher.yml
```
2. Rancher will be at: rancher.$hosted_zone

### Restore Rancher
1. Copy the backup file in /tmp directory in ec2 instance.
2. Update $restore_file variable in rancher_vars file.
```sh
ansible-playbook restore-rancher.yml
```

### Manual Rancher backup
1. Following command creates a backup and uploads to S3.
```sh
ansible-playbook backup-rancher.yml
```

### Upgrade/downgrade Rancher container image version
1. Update rancher_tag variable in rancher_vars file.
2. Run the following command:
```sh
ansible-playbook upgrade-rancher.yml
```