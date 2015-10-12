# 服务器上的Git

## 协议

###本地传输

远程仓库在该协议中的表示，就是硬盘上的另一个目录

操作
```
$git clone file:///opt/git/project.git #以网络传输数据
$git clone /opt/git/project.git        #直接复制或建立硬链接
$git remote add local_proj /opt/git/project.git #添加本地远程仓库
```

**优点**

- 简单
- 保留现有文件的权限和网络访问权限

**缺点**

- 难以控制不同位置的访问权限
- 访问速度受限于数据访问

###SSH 协议



###Git 协议



###HTTP 协议




## 在服务器上部署 Git


## 生成 SSH 公钥


## 架设服务器


## 公共访问


## GitWeb


## Gitosis


## Gitolite


## Git 守护进程


## Git 托管服务


## 小结

