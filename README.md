# ansible-role-docker

Install and configures Docker Community Edition on a CentOS (7) Linux System.

Optionally the following additional configuration can be added:
 - Create a non-root user to run the docker _client_ commands
 - Install docker-compose and configure systemd to support services based on docker-compose.yml configurations (to put in `/etc/docker/compose/<service-name>/` directories).

## Role Variables

```yaml
# Which version of Docker Community Edition (for CentOS 7) must be installed
docker_version: 18.03.1

# Should a housekeeping cronjob be configured, default: yes
docker_cleanup_cronjob: yes

# Which version of Docker Compose must be installed (from GitHub Releases), default: None
docker_compose_version: 1.21.1

# Username of the non-root linux account granted for docker client operations, default: None
docker_user: docker
```

## Credits

This project is forked from https://github.com/unprofession-al/ansible-role-docker.

This Ansible Role contains features sometimes inspired by similar works, like:

* https://github.com/geerlingguy/ansible-role-docker
* https://github.com/nickjj/ansible-docker

## License

BSD
