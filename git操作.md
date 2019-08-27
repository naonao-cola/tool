
---
    首先，你可以试着输入git，看看系统有没有安装Git：
    $ git
    The program 'git' is currently not installed. You can install it by typing:
    sudo apt-get install git
    

---
    安装完成后，还需要最后一步设置，在命令行输入：
    $ git config --global user.name "Your Name"
    $ git config --global user.email "email@example.com"
    

---
### go
##### 首先，选择一个合适的地方，创建一个空目录：
    $ mkdir learngit
##### 第二步，通过git init命令把这个目录变成Git可以管理的仓库：
    $ git init
    Initialized empty Git repository in /Users/michael/learngit/.git/
### 把文件添加到版本库
##### 第一步，用命令git add告诉Git，把文件添加到仓库：
    $ git add readme.txt //readme.txt 需要提交的文件
##### 第二步，用命令git commit告诉Git，把文件提交到仓库：
    $ git commit -m "wrote a readme file" //wrote a readme file说明内容
##### 因为commit可以一次提交很多文件，所以你可以多次add不同的文件
    $ git add file1.txt
    $ git add file2.txt file3.txt
    $ git commit -m "add 3 files."
#### 查看版本
    $ git log
    如果嫌输出信息太多，看得眼花缭乱的，可以试试加上--pretty=oneline参数：
    $ git log --pretty=oneline
##### 我们要把当前版本回退到上一个版本就可以使用git reset命令：
    $ git reset --hard HEAD^
#### 返回commit id是1094adb...
    $ git reset --hard 1094a
### 添加远程库
    $ git remote add origin git@github.com:michaelliao/learngit.git
    //把上面的michaelliao替换成的GitHub账户名
    //把上面的learngit替换成的项目名
##### 使用git 添加远程github仓库的时候提示错误：fatal: remote origin already exists. 
    1、先删除远程 Git 仓库
    $ git remote rm origin
    2、再添加远程 Git 仓库
    $ git remote add origin git@github.com:michaelliao/learngit.git
##### 下一步，就可以把本地库的所有内容推送到远程库上：
    $ git push -u origin master
#### 克隆
    $ git clone git@github.com:michaelliao/gitskills.git
