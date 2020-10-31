## 一、Git创建库

    git init 初始化库，内部生成 .git文件夹，是一个隐藏文件
    git add README.md 将会提交README.md文件
    git commit -m "first commit"   commit内容记录
    git remote add origin  git@github.com:wsgtop/test.git  添加远程仓库
    git push -u origin master

origin 是默认的远程版本库名称 

	git push origin
	上面命令表示，将当前分支推送到origin主机的对应分支。 如果当前分支只有一个追踪分支，那么主机名都可以省略。 
	
	git push 
	如果当前分支与多个主机存在追踪关系，那么这个时候-u选项会指定一个默认主机，这样后面就可以不加任何参数使用git push。
	
	git push -u origin master 
	上面命令将本地的master分支推送到origin主机，同时指定origin为默认主机，后面就可以不加任何参数使用git push了。

- 不带任何参数的git push，默认只推送当前分支，这叫做simple方式。此外，还有一种matching方式，会推送所有有对应的远程分支的本地分支。Git 2.0版本之前，默认采用matching方法，现在改为默认采用simple方式。

## 二、版本管理

- git status 查看本地仓库状态(在那个分支)，是否有修改、删除等等
- git diff   查看本地仓库和远程仓库的不同

**版本回退**

- git log 显示最近到最远的提交日志，后面添加命令--pretty=oneline，可以去除多余的信息，只看在版本好和提交信息。		
根据git log 显示的信息，可以看到HEAD。HEAD表示当前版本，上个版本表示HEAD^,上上版本表示HEAD^^,100个之前的版本表示HEAD~100

		$ git log --pretty=oneline
		abe3c45505e1a378d20db7f78c9e1ac2955139cb (HEAD -> master, origin/master, origin/HEAD) add note
		1529714b8cde87399c519c413f4d3a68baa63c03 update  .md
		efabd50e6f811da8e5b5ac4808721c44118f0c9c add newFile
		8d3613a62fcc78d2baa418c3201413d78355bca9 first commit

- git reset --hard HEAD^ 命令回退到上一个版本，也可以使用git reset --hard [版本ID]
- git reflog    查看命令历史
- git diff HEAD --[文件名] 命令可以查看工作区和版本库里面最新版本的区别

**撤销修改**

- git checkout -- file 可以丢弃工作区的修改

		$ git checkout -- readme.txt
		命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：
		一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；	
		一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

- git reset HEAD <file>可以把暂存区的修改撤销掉（unstage），重新放回工作区：

		$ git reset HEAD readme.txt
		Unstaged changes after reset:
		M	readme.txt

## 分支管理

**创建与合并分支**

- git branch -b dev 创建并切换到dev分支
- git branch dev  创建dev分支
- git checkout dev 切换到dev分支
- git merge dev 将dev分支的工作合并到master分支上    

		git merge 命令用于合并指定分支到当前分支

- git branch -d dev 删除dev分支

- git switch -c demo2 创建并切换到demo2分支
- git switch master 切换到master分支

**解决冲突**

- 当git提交代码或者合并分支出现冲突后，必须手动解决冲突，再提交
- git log --graph 可以查看分支合并图

**分支管理**

- git merge --no-off -m "merge with no-off" dev 表示合并dev分支， 其中--no-off参数表示禁用Fast forword;-m 参数表示提交的记录信息

**删除分支**
- 删除一个没有被合并的分支，使用命令 git branch -D valcan 使用大写的“D”强行删除没有被合并的分支

## 标签管理

**标签**

- git tag v1.0 新建一个标签
- git tag 查看所有标签
- git show <tagname>查看标签信息 
- git tag -a <tagname> -m "blablabla..."可以指定标签信息

- git tag -d v1.0 删除一个本地标签