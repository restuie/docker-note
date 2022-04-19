# docker-note


# 查詢所有docker容器狀態

sudo docker ps -a

# 停止所有容器

sudo docker stop $(docker ps -aq)


# 刪除所有容器
sudo docker rm $(docker ps -aq)

# 建立容器取名

sudo docker run -d -P --name web training/webapp python app.py

# 進入容器

sudo docker exec -ti "docker  CONTAINER ID" bash

# docker共用gpu

https://www.zhihu.com/question/416048158

# BUG
問題：Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json?all=1: dial unix /var/run/docker.sock: connect: permission denied

解決：sudo chmod 777 /var/run/docker.sock

# maixiang Dockerfile

docker build -t cuda-base:10.1-runtime-ssh-1.0 .

# 查詢docker brige網路

docker network inspect bridge

# yolov4 docker

https://t.ly/xBgz   Docker: Nvidia Driver, Nvidia Docker 推荐安装步骤

https://t.ly/Zoep   YOLOv4: Darknet 如何于 Docker 编译，及训练 COCO 子集 

https://t.ly/hJPU  yolov4 预训练模型yolov4.conv.137及测试模型yolov4.weights，yolov4_ncnn模型yolov4.param

https://t.ly/8Hjj  YOLOv4實作教學(使用官方repo)

https://t.ly/WSTL  Yolov4模型訓練規則和技巧

https://t.ly/J4cu  使用YOLOv4進行COCO資料集訓練
