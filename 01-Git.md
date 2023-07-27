### 1.Git配置

Git 提供了一个叫做 git config 的工具，专门用来配置或读取相应的工作环境变量。

这些环境变量，决定了 Git 在各个环节的具体工作方式和行为。这些变量可以存放在以下三个不同的地方：

- `/etc/gitconfig` 文件：系统中对所有用户都普遍适用的配置。若使用 `git config` 时用 `--system` 选项，读写的就是这个文件。
- `~/.gitconfig` 文件：用户目录下的配置文件只适用于该用户。若使用 `git config` 时用 `--global` 选项，读写的就是这个文件。
- 当前项目的 Git 目录中的配置文件（也就是工作目录中的 `.git/config` 文件）：这里的配置仅仅针对当前项目有效。每一个级别的配置都会覆盖上层的相同配置，所以 `.git/config` 里的配置会覆盖 `/etc/gitconfig` 中的同名变量。

在 Windows 系统上，Git 会找寻用户主目录下的 .gitconfig 文件。主目录即 $HOME 变量指定的目录，一般都是 C:\Documents and Settings\$USER。

此外，Git 还会尝试找寻 /etc/gitconfig 文件，只不过看当初 Git 装在什么目录，就以此作为根目录来定位。

#### 1.1 用户信息

配置个人的用户名称和电子邮件地址：

```
$ git config --global user.name "cho.kyoku"
$ git config --global user.email "zhaoxu8673@gmail.com"
```



### 2.远程仓库

#### 2.1 克隆远程仓库

 如果想将远程仓库克隆下来，需要使用 **git clone** 命令

```
git clone https://github.com/ChoKyoku/Doc.git
```

https://github.com/ChoKyoku/Doc.git 就是远程仓库的地址



#### 2.2 查看远程分支

使用 **git remote** 命令可以查看远程仓库，origin表示远程主机

使用**git remote -v** 命令可以查看远程仓库详细信息，包括远程仓库的地址

![](Images\01-Git\Git-001.jpg)

![](Images\01-Git\Git-002.jpg)



#### 2.3 Git分支管理

##### 2.3.1 列出分支

在git中，使用**git branch** 命令列出所有分支，没有参数的时候就列出本地所有的分支

![](Images/01-Git/Git-003.jpg)

##### 2.3.2 创建分支

在git中，使用 **git branch 分支名** 的方式来创建新的分支。

![](Images\01-Git\Git-004.jpg)

##### 2.3.3 切换分支

使用**git checkout 分支名** 的方式来切换到想要的分支。切换好新的分支之后，所有的内容也全部都更换成新的分支的内容了。

![](Images\01-Git\Git-005.jpg)

##### 2.3.4 合并分支

在git中，如果想将其他的分支内容合并到当前的分支中的话可以使用 **git merge** 命令

**语法:git merge oBranch**

**作用:将oBranch的内容合并到当前分支中来**

![](Images\01-Git\Git-006.jpg)

### 3.常用操作

#### 3.1 git clone

用于将远程仓库的内容克隆到本地

**语法: git clone [url]**

#### 3.2 git add

可将文件添加到暂存区(一个或多个文件)

**语法:git add [file1] [file2] ...**

**git add -A** : 用于将当前目录下的所有文件都添加到暂存区

#### 3.3 git commit

将暂存区中的内容添加到本地仓库中

语法: git commit -m [message]

   message : 可以是一些备注信息

git commit -a : 执行该指令时，修改文件后不需要执行git add命令，直接来提交

#### 3.4 git push

用于将本地仓库中的内容推送到远程仓库中

语法: git push <远程仓库地址> <本地分支>

​          git push origin cho.kyoku

#### 3.5 git checkout

#### 3.6 git pull