# nodered-ansible
Technical assessment for flugel.it. Provision nodered instance using Ansible.

## Using Vagrant.
- To test, clone repo and run vagrant up --provider=docker.

- To access nodered, localhost:1880

- To destroy, run vagrant destroy.

## Using Terraform with AWS as provider.
1. Add values for variables in the config.tfvars.

```hcl
access_key = ""
secret_key = ""
key_name = ""
ssh_key_private = ""
python_interpreter = ""
```

2. To run you need to execute:

```bash
$ terraform init 
$ terraform plan -var-file="config.tfvars"
$ terraform apply -var-file="config.tfvars"
```

3. To destroy you need to execute:

```bash
$ terraform destroy -var-file="config.tfvars"
```