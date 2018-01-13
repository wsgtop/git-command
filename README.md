# Git创建库
- git init 
- git add README.md  
- git commit -m "first commit"
- git remote add origin git@github.com:wsgtop/test.git
- git push -u origin master

----
    git init 初始化库，内部生成 .git文件夹，是一个隐藏文件
    git add README.md 将会提交README.md文件
    git commit -m "first commit"   commit内容记录
    git remote add origin    添加远程仓库
    git push -u origin master

origin 是默认的远程版本库名称 

	git push origin
	
	上面命令表示，将当前分支推送到origin主机的对应分支。 如果当前分支只有一个追踪分支，那么主机名都可以省略。 
	
	git push 
	
	如果当前分支与多个主机存在追踪关系，那么这个时候-u选项会指定一个默认主机，这样后面就可以不加任何参数使用git push。
	
	git push -u origin master 
	
	上面命令将本地的master分支推送到origin主机，同时指定origin为默认主机，后面就可以不加任何参数使用git push了。

- 不带任何参数的git push，默认只推送当前分支，这叫做simple方式。此外，还有一种matching方式，会推送所有有对应的远程分支的本地分支。Git 2.0版本之前，默认采用matching方法，现在改为默认采用simple方式。
