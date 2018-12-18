# supervisord-docker

This Dockerfile installs the latest [Supervisor][1].

# Usage

## Default supervisord.conf

```bash
$ docker run -d \
    --name "my_default_supervisord" \
    -p 9001:9001 \
    ef9n/supervisord:0.1.0
```

Now you can access the Supervisor UI at 'http://localhost:9001' from your host system.

## Custom supervisor configurations

```bash
$ docker run \
    --name "my_custom_supervisord" \
    -p 9001:9001 \
    -v <custom_supervisor_directory>:/etc/supervisor \
    ef9n/supervisord:0.1.0
```

[1]: http://supervisord.org/
