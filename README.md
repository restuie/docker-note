# docker-note


# 查詢所有docker容器狀態
sudo docker ps -a

＃ 停止所有容器
sudo docker stop $(docker ps -aq)


# 刪除所有容器
sudo docker rm $(docker ps -aq)

# 建立容器取名

sudo docker run -d -P --name web training/webapp python app.py

# 進入容器

sudo docker exec -ti "docker  CONTAINER ID" bash


# BUG
問題：Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json?all=1: dial unix /var/run/docker.sock: connect: permission denied

解決：sudo chmod 777 /var/run/docker.sock
