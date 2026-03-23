# ansible_galaxy_nginx_installation

Ansible role to install and configure Nginx, then publish `index.html`.

## Requirements

- Ubuntu/Debian target host
- `become: true`

## Role Variables

See `defaults/main.yml`:

- `nginx_package`: package name (default: `nginx`)
- `nginx_service`: service name (default: `nginx`)
- `nginx_web_root`: web root (default: `/var/www/html`)
- `nginx_index_src`: source file from role `files/` (default: `index.html`)

## Example Playbook

```yaml
---
- hosts: server-01
  become: true
  roles:
    - role: kodal035.ansible_galaxy_nginx_installation
```
