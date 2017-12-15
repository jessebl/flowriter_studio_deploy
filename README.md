# Ansible deployment for flowriter_studio

Using Ansible with root/sudo privilege on CentOS, deploy flowriter_studio.
Defaults to running on port 8000, and is configured as a `systemd` service.

## System Requirements

* **OS:** CentOS 7
* **Memory:** >= 1024 MB (as of ff92fef8d87848fdbf80fcd617abe80a9a3809fd)

## Usage

```bash
ansible-playbook -i production deploy.yml
```

To deploy a specific version of the app, you can pass the `git_branch` variable
to Ansible:


```bash
# Deploy the develop branch
ansible-playbook -i production deploy.yml --extra-vars "git_branch=develop"
```
