# Docker 指令

## image 操作

```bash
# 列出所有的 image
sudo docker images
# 使用 Dockerfile build image
sudo docker build -t myweb .
```

## Container 操作

```bash
# 列出所有的containers
sudo docker ps -a
# 停止 container
sudo docker stop [CONTAINER ID]
# 刪除 container
sudo docker rm [CONTAINER ID]
# 建立 container ,作業範例
sudo docker run -id --name myweb -p 8080:80 --volume mywebVolume:/var/www/ myweb
# 建立 container 使用別的 container 的 volume ,作業範例
sudo docker run -id --name myweb2 -p 8081:80 --volumes-from myweb myweb
# 進入 container
docker exec -it myweb bash
# 在 container 內的離開
exit

```

## volume 操作

```
# 列出所有的volume
sudo docker volume ls
```