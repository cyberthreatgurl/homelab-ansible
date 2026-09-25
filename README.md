# Homelab Ansible Automation

Ansible playbooks and configuration for homelab services:
- **`bootstrap-pihole.yml`**: Bootstrap the `ansible-deploy` service account on Pi-hole.
- **`bootstrap-docker-server.yml`**: Bootstrap the `ansible-deploy` service account on Docker host.
- **`configure-pihole-ssl.yml`**: Request and configure SSL certificates on Pi-hole from the internal step-ca.
- **`step-ca-playbook.yml`**: Deploy step-ca private CA on Kubernetes.

## Layout

```
homelab-ansible/
├── inventory/
│   ├── hosts.ini                Homelab inventory (k8s, pihole_servers, docker_servers, webmin_servers)
│   └── group_vars/
│       └── all.yml              Global variables & authorized admin keys
├── playbooks/
│   ├── bootstrap-docker-server.yml
│   ├── bootstrap-pihole.yml
│   ├── configure-pihole-ssl.yml
│   └── step-ca-playbook.yml
├── ansible.cfg
└── README.md
```

## Running Playbooks

```bash
# Dry run
ansible-playbook playbooks/configure-pihole-ssl.yml --check --diff

# Execute
ansible-playbook playbooks/configure-pihole-ssl.yml
```
