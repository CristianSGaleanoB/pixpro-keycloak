# Keycloak Configuration

This repository is used to run the basic Keycloak configuration for the whole team.

To run it, use the following command:

```bash
docker compose up -d
```

To stop all containers and restart them, use the following command:

```bash
docker compose down -v
```

To export config:

```bash
docker exec -it <container-name> /opt/keycloak/bin/kc.sh export --dir /tmp/export --realm pixpro-realm
docker cp keycloak:/tmp/export /tmp/temp-export
sudo chown -R $USER:$USER /tmp/temp-export
mv /tmp/temp-export ./export
```
