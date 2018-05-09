# Changelog for ansible-role-docker

## [Unreleased]

TODO: Are all the Jenkins Requirements covered by v1.2.0?

## v1.2.0 - 2018-05-09

### Added

- Support for multiple docker users [GH-2]
- A basic README file
- A CHANGELOG file

### Fixed

- Use `systemd` module to run daemon-reload, instead of a raw `command` task (see also swisstxt/ansible-env-cargo#30)
  Note: handler name "run daemon-reload" is kept unchanged for backwards compatibilty (but might be renamed as something like "reload systemd" in a future release

## v1.1.0 - 2018-05-02

### Added

- Docker-compose **optional** installation
- **optional** creation of a non-root linux user granted to execute `docker` clients
- Support for multiple docker-composed-based systemd services (e.g. `docker-compose@myservice` (only if docker-compose is installed)
- A 'docker cleanup' cron job (enabled by default)

### Changed

- Install Docker Community Edition from new site: https://download.docker.com

### Removed

- Support for CentOS 6

## v1.0.x - 2017-..-..

A bunch of changes added to satisfy SWISSTXT Kubernetes Platform requirements

:warning: These changes are not part of this git repo history.

## v1.0.0 - 2016-10-16

Initial Release (forked from [unprofession-al](https://github.com/unprofession-al/ansible-role-docker/tree/v1.0.0) original ansible role)
