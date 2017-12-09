# Ansible deployment for flowriter_studio

Using Ansible with root/sudo privilege on CentOS and Ubuntu, deploy
flowriter_studio. Defaults to running on port 8000, and is configured as a
`systemd` service.

## Usage

```bash
ansible-playbook -i production deploy.yml
```
