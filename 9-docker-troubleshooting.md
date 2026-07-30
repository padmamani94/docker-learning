# Docker Troubleshooting

## Problem

Docker service is not running.

## Solution

```bash
sudo systemctl start docker
```

---

## Problem

Permission denied while running Docker.

## Solution

```bash
sudo usermod -aG docker $USER
newgrp docker
```

---

## Problem

Port already in use.

## Solution

```bash
sudo lsof -i :80
```

Stop the process using the port or run the container on another port.

---

## Problem

Container exits immediately.

## Solution

```bash
docker logs <container-id>
```

Review the logs to identify the application error.
