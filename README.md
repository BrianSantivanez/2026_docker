# 2026_docker

Create:
- One Mysql container
- One phpMyAdmin container
- One volume in the root directory

## Commands
```
docker compose up -d
```
```
docker compose down -v
```

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
