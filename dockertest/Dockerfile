FROM nvidia/cuda:10.1-cudnn8-runtime-ubuntu18.04
MAINTAINER author<pan_yong_feng@hotmail.com>
RUN echo "export LANG=C.UTF-8" >>/etc/profile \
&& mkdir -p /.script \
&& cp /etc/apt/sources.list /etc/apt/sources.list.bak \
#&& echo "deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse\n\
#deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse\n\
#deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse\n\
#deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse" >/etc/apt/sources.list \
&& apt-get update \
&& apt-get install vim openssh-server iputils-ping wget curl -y \
&& sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/g' /etc/ssh/sshd_config \
&& echo "root:123456" | chpasswd \
&& echo "\
printf '\\\n'\n\
printf '\\\033[0;34m'\n\
printf ' Welcome to maixiang \\\n'\n\
printf '__        __     _      __  __    __  __      _      ___    __   ______        \\\n'\n\
printf '| \      / |    /_\    |__| \ \  / / |__|    / \    |   \  | |  |  ____|       \\\n'\n\
printf '||\\    //||   / _ \    ||   \ \/ /   ||    / _ \   |  _ \ | |  | |   __       \\\n'\n\
printf '|| \\_ // ||  / ___ \   ||   / /\ \   ||   / ___ \  | | \ \| |  | |___||       \\\n'\n\
printf '||  \_//  || /_/   \_\ |__| /_/  \_\ |__| /_/   \_\ |_|  \___|  |______|       \\\n'\n\
printf '\\\033[0m'\n\
printf '\\\n'\n\
" >>/etc/update-motd.d/10-help-text
ADD ssh_start.sh /.script/
RUN chmod +x /.script/*
