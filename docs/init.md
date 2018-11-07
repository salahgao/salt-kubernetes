
# 系统环境初始化

## 1.安装Docker

第一步：使用国内Docker源
```
[root@linux-node1 ~]# cd /etc/yum.repos.d/
[root@linux-node1 yum.repos.d]# wget \
 https://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
 ```

第二步：Docker安装：
```
[root@linux-node1 ~]# yum install -y docker-ce
```

第三步：启动后台进程：
```
[root@linux-node1 ~]# systemctl start docker
```

## 2.准备部署目录
```
mkdir -p /opt/kubernetes/{cfg,bin,ssl,log}
```
```
[root@linux-node1 ~]# cat .bash_profile
# .bash_profile

# Get the aliases and functions
if [ -f ~/.bashrc ]; then
	. ~/.bashrc
fi

# User specific environment and startup programs

PATH=$PATH:$HOME/bin:/opt/kubernetes/bin

export PATH
```

## 3.准备软件包
```
https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG-1.10.md

cd /usr/local/src
wget https://dl.k8s.io/v1.10.9/kubernetes.tar.gz
wget https://dl.k8s.io/v1.10.9/kubernetes-client-linux-amd64.tar.gz
wget https://dl.k8s.io/v1.10.9/kubernetes-server-linux-amd64.tar.gz
wget https://dl.k8s.io/v1.10.9/kubernetes-node-linux-amd64.tar.gz
```

## 4.解压软件包
```
 # tar zxf kubernetes.tar.gz 
 # tar zxf kubernetes-server-linux-amd64.tar.gz 
 # tar zxf kubernetes-client-linux-amd64.tar.gz
 # tar zxf kubernetes-node-linux-amd64.tar.gz
```



