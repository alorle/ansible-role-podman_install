# Podman Install

Ansible role to install podman on Debian based distros using [home:alvistack](https://build.opensuse.org/project/show/home:alvistack) repository.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see [defaults/main.yml](defaults/main.yml)):

| Variable                  | Description                                       | Default value |
| ------------------------- | ------------------------------------------------- | ------------- |
| `podman_install_packages` | List of packages to be installed within the role. | `["podman"]`  |
| `podman_service_state`    | Podman service's state after role execution.      | `started`     |
| `podman_service_enabled`  | Wheter to enable podman service at boot.          | `true`        |

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
