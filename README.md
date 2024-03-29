# Podman Install

Ansible role to install podman on Debian 12 and Ubuntu 22.04 using [devel:kubic:libcontainers/unstable](https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/unstable) repository.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see [defaults/main.yml](defaults/main.yml)):

| Variable                  | Description                                       | Default value |
| ------------------------- | ------------------------------------------------- | ------------- |
| `podman_install_packages` | List of packages to be installed within the role. | `["podman"]`  |

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  vars:
    podman_install_packages:
      - podman>=4.4
      - crun
  roles:
    - alorle.podman_install
```

## License

MIT
