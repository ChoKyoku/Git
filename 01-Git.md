### 1.远程仓库

#### 1.1 克隆远程仓库

 如果想将远程仓库克隆下来，需要使用 **git clone** 命令

```
git clone https://github.com/ChoKyoku/Doc.git
```

https://github.com/ChoKyoku/Doc.git 就是远程仓库的地址



#### 1.2 查看远程分支

使用 **git remote** 命令可以查看远程仓库，origin表示远程主机

使用**git remote -v** 命令可以查看远程仓库详细信息，包括远程仓库的地址

![](Images\01-Git\Git-001.jpg)

![](Images\01-Git\Git-002.jpg)



#### 1.3 Git分支管理

##### 1.3.1 列出分支

在git中，使用**git branch** 命令列出所有分支，没有参数的时候就列出本地所有的分支

![](Images/01-Git/Git-003.jpg)

##### 1.3.2 创建分支

在git中，使用 **git branch 分支名** 的方式来创建新的分支。

![](Images\01-Git\Git-004.jpg)

##### 1.3.3 切换分支

使用**git checkout 分支名** 的方式来切换到想要的分支。切换好新的分支之后，所有的内容也全部都更换成新的分支的内容了。

![](Images\01-Git\Git-005.jpg)

##### 1.3.4 合并分支

在git中，如果想将其他的分支内容合并到当前的分支中的话可以使用 **git merge** 命令

**语法:git merge oBranch**

**作用:将oBranch的内容合并到当前分支中来**

![](Images\01-Git\Git-006.jpg)