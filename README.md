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
###### 已映射端口
```
18022:22
8888:8888
```
映射22端口 通过ssh访问容器
映射8888端口是为了访问jupyter notebook
映射端口时需注意本地端口不要被占用

###### 已映射文件
```
./:/root/workspace
```
所以当前目录文件都在docker的/root/workspace中 

###### 修改文件和端口映射
```
修改docker-compose.yml 配置文件
docker-compose up -d 重新启动就可以了
```

### 已安装环境及工具
* Anaconda3
* ssh
* tmux

Enjoy Yourself
