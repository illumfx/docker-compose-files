# 🐋 My collection of Docker-Compose files

### Traefik as a proxy
Traefik checks each container name uses its value as an subdomain. If you want to change this behaviour but not change the container name, add the following labels:

```yaml
- "traefik.enable=true"
- "traefik.http.routers.CONTAINER_NAME.rule=Host(`YOUR_HOST`)"
```