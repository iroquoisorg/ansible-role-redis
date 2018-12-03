# redis

[![Build Status](https://travis-ci.com/iroquoisorg/ansible-role-redis.svg?branch=master)](https://travis-ci.com/iroquoisorg/ansible-role-memcached)

Ansible role for redis

This role was prepared and tested for Ubuntu 16.04.

# Installation

`$ ansible-galaxy install iroquoisorg.redis`

# Default settings

```

redis_port: 6379
redis_bind_interface: 127.0.0.1
redis_unixsocket: ''
redis_timeout: 300

redis_loglevel: "notice"
redis_logfile: /var/log/redis/redis-server.log

redis_databases: 16
redis_save:
  - 900 1
  - 300 10
  - 60 10000

redis_rdbcompression: "yes"
redis_dbfilename: dump.rdb
redis_dbdir: /var/lib/redis

redis_maxmemory: 0
redis_maxmemory_policy: "noeviction"
redis_maxmemory_samples: 5

redis_appendonly: "no"
redis_appendfsync: "everysec"

redis_extra_instances: []

# Add extra include files for local configuration/overrides.
redis_includes: []

```

# Development

Please check [development guide](DEVELOPMENT.md) for details about developing and testing this role.
