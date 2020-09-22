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
```
