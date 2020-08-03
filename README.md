# Ansible docker discovery

Deploy Traefik via Docker.
It manage rules `3000/tcp` and `8000/tcp` for automatic discovery and has ui on `8080/tcp` port.

## Depend

- docker
- python-docker-py | python-docker | python3-docker

## Role Variables

`docker_discovery_enabled: false` - enable or disable this role.
`docker_discovery_image: traefik` - name of image.
`docker_discovery_version` - version of image.
`docker_discovery: {}` - container and network description to create or update.

To see defaults please view defailts/main.yml

## Example Playbook

```yml
- hosts: localhost
  remote_user: root
  become: yes
  roles:
    - ansible-docker-discovery
```

## License

MIT License

## Author Information

Carrol Cox <carrol@protonmail.com>
