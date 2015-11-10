---
layout: page
title: Git Handbook
---

从官网下载git，安装到本地window 7系统上，见识一下git的魅力，全指令输入是，命令行的模式，特别是gitbash
里面有各种指令，功能强大，我在想如果做成界面，那要需要多少界面，由此可见其指令之多，功能强大。


git的原理是分支，主分支和分支，本机做好的代码，提交到本地分支，然后提交到主分支，可以合并主分支。


分布式的版本控制加上指令的交互，用着很舒服。

1.本机git使用

安装window版本的git后，开始操作，启动gitbash.ext,进入命令行

创建新目录learngit,进入此目录

git init 初始化仓库

git add file 添加文件，只是添加到缓冲区，还没有提交到库(常用)

git commint -m " description"  提交（常用）

git log 查看修改记录(常用)

git status 查看本地仓库状态(常用)

git diff 查看修改(常用)

git rm file 删除文件(常用)

git reset HEAD file 重置文件(常用)

git tag 打标签


2.github上建仓库操作

在github.com上注册一个账号，就有了自己的一亩三分地，要好好滴写代码，开发自己的仓库。

ssh-keygen -t rsa -C "your email"

生成公匙和私匙，把公匙添加到github上的sshkey列表里，建立本机和服务器的认证

ssh -vT git@github.com  检查是否能用ssh和github通信

git remote add origin git@github.com:gongpu/learngit.git(修改成自己的github仓库)   添加远程仓库

git push origin master  提交到主分支（常用）

git clone git@github.com:gongpu/learngit.git

从远程仓库克隆一份代码到本地（常用),git的仓库千千万万，浏览和学习别人的代码，会很受益的。


3.git分支的操作

git brancn 查看分支 (常用)

git  branch dev 创建分支 (常用)

git checkout branch dev 检出分支的代码 (常用)

git checout -b dev  创建分支并指向分支（常用）

git merge dev 合并分支 (常用)

git branch -d dev 删除已合并分分支

git branch -D dev 强制删除，删除没有合并的分支

git checkout branch 分支是由指针操作，移动到不同分支 ，检出代码(常用)


（重要、常用）

场景多人协作，别人先修改了文件，你再提交的时候git会提示有冲突，先pull解决解决冲突后再提交

如果pull失败，先建立连接

git branch --set-upstream dev origin/dev

git2.0新指令 git branch --set-upstream-to dev origin/dev

git pull拿下来最新的代码

手动解决冲突后，git push提交代码


修复bug的的时候，开新的分支，保存现场的指令就用到了

git stash 保存开发现场（常用）

git stash list 查看

git stash pop  恢复现场 或 git stash apply,然后删除保存的现场git stash drop


分支的管理 master主分支（同步）、dev开发分支（同步）、bug分支（不一定同步）、feature分支(看情况而定)

指令的配置,用来偷懒的指令

git config --global alias.st status 用st代替status

git config --global alias.commit ci

git config --global alias.branch br

.gitignore 文件，定义要忽略的文件

pull request 在github.com上，提交你在fork分支里的修改，如果被原作者同意接受，就可以合并到主分支了。

github分享，协作的好平台，好好利用，不要搞破坏，这对大家都有好处。

question 1 :github不支持GBK编码，所以你的项目采用UTF-8编码方式，以防上传出现中文乱码问题

转载请在文章明显位置放置本文的链接，谢谢！如有疑问，欢迎来信交流学习探讨。

