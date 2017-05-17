
#### 初识docker
    学习golang的时候，初识docker的大名，但一直没有去深入了解它。最近才有心思去陈定下来研究，遂把自己的一些学习心得记录下来，整理成册，以供大家参考，学习，交流。
    
    
##### 一.准备工作
    虚拟机一台，系统ubuntu 14.04 内存2G
    安装openSSH  网络为桥接网络，IP 192.168.0.104
    安装curl
    
##### 二.安装docker
###### 2.1 下载
    docker的官网地址为： www.docker.com
    下载地址为：https://store.docker.com/editions/community/docker-ce-server-ubuntu
    
###### 2.2 更新apt-get资源库
    step1: 执行curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    step2: 执行sudo add-apt-repository \
                    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
                    $(lsb_release -cs) \
                    stable"
    step3: 执行sudo apt-get update
    
###### 2.3 通过apt-get安装docker
    执行：sudo apt-get -y install docker-ce
    等待安装完成。如果不能正常安装，请翻墙再试试

###### 2.4 测试是否安装正常
    运行官方镜像 helloworld
    sudo docker run hello-world  等待下载并启动
    如果运行成，则如下图：
 <img src=../img/hello.png/>
    