# MachineLearning-Docker
用Docker构建机器学习环境

### 构建目的
使程序的运行环境通过Docker来管理，再也不用为环境问题配置半天。提高开发，共享效率。

### 使用方法

###### 依赖
* docker-compose


###### 开启容器
```
git clone https://github.com/smbeli/MachineLearning-Docker.git
cd MachineLearning-Docker
docker-compose up -d
```

###### 登录到容器
```
ssh root@localhost -p 18022
password 123456
```

###### 修改文件和端口映射
```
修改docker-compose.yml 配置文件
docker-compose up -d 重新启动就可以了
```

### 已安装环境及工具
* Anaconda3
* tmux
