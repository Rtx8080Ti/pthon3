# 2019年12月26日
Ubuntu 19.10 & Windows 1909 & macOS 10.15.2
python 3.7.5

今日目标：通过git打通Ubuntu & Windows  & macOS 平台

## 问题1：Ubuntu终端不识别 python 命令，提醒可以安装，提醒已安装python3，但是需要执行 python3 命令。
平台：Ubuntu 19.10 

解决办法：

Ubuntu19.10切换python3和python2

切换Python3为默认版本：

sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 100

sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 150

切换Python2为默认版本：

sudo update-alternatives --config python

## 问题2：Ubuntu下如何使用git？
平台：Ubuntu 19.10 

解决办法：

[转载来自](http://www.sohu.com/a/224286147_185201)

1.安装Git for Linux

下载和安装Git for Linux：

sudo apt-get install git

2.配置GitHub

配置GitHub用户，使用下列两个命令，把“user_name”换成你的GitHub用户名，把“email_id”换成你用来创建GitHub帐户的电子邮件ID。

git config --global user.name "user_name" git config --global user.email "email_id"

3.创建本地仓库

在系统上创建一个文件夹。该文件夹将充当本地仓库，以后会被推送到GitHub网站。使用下列命令：

git init Mytest

如果仓库成功创建，那么你会看到下列行：

Initialized empty Git repository in /home/akshay/Mytest/.git/

这一行可能不一样，具体取决于你的系统。

所以这里，Mytest是创建的文件夹，“init”使该文件夹成为GitHub仓库。将目录改成这个新创建的文件夹：

cd Mytest

4.创建描述仓库的README文件

现在创建一个README文件，输入一些文本，比如“this is a git setup on linux”。README文件通常用来描述仓库含有的内容或项目的性质。例子如下：

gedit README

可以使用其他任何文本编辑器，我使用gedit。README文件的内容如下：

This is a git repo

5.将仓库文件添加到索引

这是个重要的步骤。这一步，我们把需要推送到GitHub网站的所有内容添加到索引中。这些内容可能是你首次添加到仓库中的文本文件或程序，也可能是添加已经存在，但出现了一些变更的文件（更新颖的版本/经过更新的版本）。

使用下列命令，添加到索引中：

git add README.md

注意：“git add”命令可用于将任何数量的文件和文件夹添加到索引中。本文中出现的索引是指类似缓冲器的空间，用来存放要添加到Git仓库中的文件/文件夹。

6.提交对index所作的变更

一旦所有文件添加完毕，我们就可以提交了。这意味着，我们最终敲定了要添加及/或变更的内容，现在它们已准备好上传到我们的仓库。使用该命令：

git commit -m "some_message"

上述命令中的“some_message”可能是任何简单的信息，比如“my first commit”或“edit in readme”等等。

7.在GitHub上创建仓库

在GitHub上创建仓库。请注意：仓库名称应该与本地系统上的仓库名称一样。这里，它将是“Mytest”。为此，登录到你在 github.com 上的帐户。然后点击页面右上角的“+”符号，选择“create new repository”。填写细节，如下图所示，点击“create repository”按钮。

一旦创建完毕，我们可以将本地仓库的内容推送到你个人简档（profile）中的GitHub仓库。使用该命令，连接到GitHub上的仓库：

重要告知：在运行该命令之前，确保把路径中的“user_name”和“Mytest”换成了你的Github用户名和文件夹！

git remote add origin https://github.com/user.name/Mytest.git

8.将本地仓库中的文件推送到GitHub仓库

最后一步是，使用该命令，将本地仓库的内容推送到远程主机仓库（GitHub）：

git push origin master

输入登录用户信息[用户名和密码] 。

所以，这将“Mytest”文件夹（我的本地仓库）中的所有内容添加到GitHub。针对后续项目或如果要创建仓库，你可以直接从第3步开始。最后，如果你登录到GitHub帐户，点击你的Mytest仓库，就会发现 README 已被上传。

备注:将远程主机仓库（GitHub）的内容下载更新到本地仓库：

git pull origin master


