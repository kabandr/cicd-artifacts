# Running cAdvisor in Docker

```
sudo docker run -d \
  --name=cadvisor \
  --privileged=true \
  --volume=/:/rootfs:ro \
  --volume=/var/run:/var/run:rw \
  --volume=/sys:/sys:ro \
  --volume=/var/lib/docker/:/var/lib/docker:ro \
  --volume=/dev/disk/:/dev/disk:ro \
  --publish=8080:8080 \
  --restart=always \
  google/cadvisor:latest

```
