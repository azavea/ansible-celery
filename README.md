# ansible-celery

An Ansible role for installing [Celery](http://www.celeryproject.org/).

## Role Variables

- `celery_version` - Celery version
- `celery_dir` - Directory for Celery worker to execute from (default: `/var/lib/celery`)
- `celery_bin` - Path to Celery binary (default: `/usr/local/bin/celery`)
- `celery_start_on` - Upstart `start on` stanza (default: `local-filesystems and net-device-up IFACE!=lo`)
- `celery_app` - Celery application name (default: `proj`)
- `celery_broker_url` - Celery broker URL (default: `redis://localhost:6379/0`)
- `celery_log_level` - Celery worker log level (default: `info`)
- `celery_log` - Celery log path (default: `/var/log/beaver.log`)
- `celery_log_rotate_count` - Celery log rotation count (default: `5`)
- `celery_log_rotate_interval` - Celery log rotation interval (default: `daily`)

## Example Playbook

Currently, this role is highly dependent on Redis being the Celery broker.

See the [examples](./examples/) directory for more details.
