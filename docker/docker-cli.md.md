# Docker 常用命令

```shell
# 查看 image
docker images

# 查看容器实例
docker ps [-a]

# 构建 image
docker build -t image_name path/to/Dockerfile

# 运行 docker 容器实例
docker run --rm -dp host_port:container_port image command

# 运行的容器中打开 shell
docker exec -it <container_name> <sh>

# 停止/开始/删除容器
docker start/stop/rm container_name

# 删除镜像
docker rmi IMAGE
```
