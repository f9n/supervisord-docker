# supervisord-docker

This Dockerfile installs the latest [Supervisor][1].

# Usage

## Default supervisord.conf

```bash
$ docker run -d \
    --name "my_default_supervisord" \
    -p 9001:9001 \
    f9n/supervisord:0.1.0
```

Now you can access the Supervisor UI at 'http://localhost:9001' from your host system.

## Custom supervisord.conf

```bash
$ docker run \
    --name "my_custom_supervisord" \
    -p 9001:9001 \
    -v <custom_supervisor_directory>:/etc/supervisor \
    f9n/supervisord:0.1.0
```

[1]: http://supervisord.org/
