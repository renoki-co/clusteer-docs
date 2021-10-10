# Docker

The package also comes with Docker for the server part. You can easily run the server in Docker and have the PHP application query through the exposed REST API.

[Tags are available to Quay.io](https://quay.io/repository/renokico/clusteer)

```bash
docker run -p 8080:8080 -e DEBUG=1 quay.io/renokico/clusteer:3.0
```
