# 2026_docker

Create:
- One Postgres container
- One phpMyAdmin container
- One volume in the default directory

## Commands
```
docker compose up -d
```
```
docker compose down -v
```

## Create server from pgAdmin

To create a server all data are inside of docker network so is necessary to use internal data (container names instead IPs, internal ports instead external ports, etc.)

    General: 
        - Name: YOUR_SERVER_NAME
    Connection: 
        - Hostname: bd_postgres
        - Port: 5432
        - Maintenace Database: postgres
        - Username: postgres
        - Password: root

## Clear memory
```
# 1. Clean up everything Docker is not currently using (dangling images, caches, etc.)
docker system prune -a --volumes

# 2. Clean up old APT packages in Ubuntu
sudo apt autoremove --purge
sudo apt clean

# 3. Clean up system journald logs that can sometimes take up a lot of space
sudo journalctl --vacuum-time=1d
```
