## 1.github 创建 仓库

## 2.在本地文件夹下初始话本地仓库

```shell
git init
```

## 3.添加文件（将文件放入暂存区）

```shell
git add .
git commit -m "the first"
```

### 设置git邮箱和用户名

```shell
# 设置全局的用户名和邮箱
全局的 Git 用户名和密码将会和你系统上所有没有指定项目及标识的项目上的 commits 相关联。

想要设置全局 commit 名字和邮件地址，运行git config命令，加上--global选项：

git config --global user.name "Your Name"
git config --global user.email "youremail@yourdomain.com"

# 查看 配置信息
$ git config --list | grep user
user.email=1583662668@qq.com
user.name=wp
# 这个命令将这些值保存在全局配置文件,~/.gitconfig：
$ cat ~/.gitconfig
[user]
        email = 1583662668@qq.com
        name = wp
[http]
        sslVerify = false
[filter "lfs"]
        clean = git-lfs clean -- %f
        smudge = git-lfs smudge -- %f
        process = git-lfs filter-process
        required = true

```

## 4.设置公钥

```shell
ssh-keygen -t rsa -C "1583662668@qq.com"
# C:\Users\QM_WP\.ssh
```

![image-20221014113854302](D:\MyDocument\PythonProject\JupyterWorkBase\同步到github的步骤.assets\image-20221014113854302.png)

### 拷贝*.pub 文件中的内容到 github中

![image-20221014114233630](D:\MyDocument\PythonProject\JupyterWorkBase\同步到github的步骤.assets\image-20221014114233630.png)

## 5.绑定远程仓库

![image-20221014114307185](D:\MyDocument\PythonProject\JupyterWorkBase\同步到github的步骤.assets\image-20221014114307185.png)

> 绑定本地文件夹与远程仓库

```shell
git remote add origin [SSH]
```

> 推送

```shell
git push -u origin master

# git push -f -u origin master # 强行把本地库 覆盖到 远程库
```











