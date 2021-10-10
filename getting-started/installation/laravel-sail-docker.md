# Laravel Sail (Docker)

For Laravel Sail, you might use the [Docker](docker.md) containers and add a new service in your `docker-compose.yaml` file:

```yaml
# For more information: https://laravel.com/docs/sail
version: '3'
services:
    # ...

    clusteer:
        image: 'quay.io/renokico/clusteer:latest-16-alpine'
        environment:
            DEBUG: '1'
            MAX_BROWSERS: '1'
        ports:
            - '${CLUSTEER_PORT:-8080}:8080'
        networks:
            - sail

networks:
    sail:
        driver: bridge
```
