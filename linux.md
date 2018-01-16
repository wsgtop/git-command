# linux命令
---

## 文件操作

    ls      查看当前目录文件
	ls -a   查看当前目录所有文件,包括隐藏文件
	ls -l   命令来查看当前目录文件的属性
	ls -al 可以查看当前目录下的所有文件，包括隐藏文件，是命令ls -a与ls -l的合并
	touch   touch可以用于创建二进制文件，用法非常简单。用法：touch+文件名，touch与文件名之间一定要有空格
	mkdir   mkdir可以创建文件夹，用法非常简单，用法：mkdir+文件夹名字，mkdir与文件名之间一定要有空格
    rm      移除文件 rm +文件名
    rmdir   移除空文件夹 rmdir +文件名
    rm -rf  向下递归并且强行删除文件或文件夹 
			-r 就是向下递归，不管有多少级目录，一并删除
            -f 就是直接强行删除，不作任何提示的意思
			1. 删除文件夹实例：
			rm -rf /var/log/httpd/access
			将会删除/var/log/httpd/access目录以及其下所有文件、文件夹
			2. 删除文件使用实例：
			rm -f /var/log/httpd/access.log
			将会强制删除/var/log/httpd/access.log这个文件

---
## 11个window连接linux的问题

1. 获取linux ipAdress             
登录linux ，命令ifconfig获取<br><br>
2. 怎么连接linux                  
通过putty对linux进行window连接<br><br>
3. 怎么传送数据到linux        
怎么使用FTP传送数据<br><br>
4. 怎么解压（zip）、压缩(unzip)文件                
<br><br>
5. 怎么移动文件</br>
使用mv可以移动文件和对文件进行重命名</br>
mv + <filename\path> + <new filename\path> <br>
如果第二个参数是一个目录，这是一个移动文件的命令；如果第二个参数是一个目录且目录的结尾是一个名字，这是一个移动并且重命名的命令</br>
例如：mv /a /b/c/   将当前路径下a移动到当前路径下/b/c下
例如：mv /a /b/c/d   将当前路径下a移动到当前路径下/b/c下,并且重命名为d <br><br>
6. 怎么安装node.js
<br><br>
7. 怎么安装pm2<br>
安装node.js后使用命令可以直接安装PM2   ==>     npm install pm2 -g <br><br>  
8. 怎么编辑文件<br>
使用vim ＋文件路径即可使用vim编辑器打开文件<br>
例如： vim  /a.txt 使用vim打开当前目录下a.txt文件<br><br>
9. 数据库<br>
通过sqlyog连接linux数据库<br><br>
10. 文件（文件夹）重命名  
mv + 原文件（文件夹）名 + 新文件（文件夹）名，以空格代表 [+]即可 </br>
例如： mv a b    将当前文件路径下a文件（或文件夹）重命名为b文件（文件夹） </br>
例如： mv a.txt b.txt      将当前文件路径下a.txt文件重命名为b.txt文件 </br>	
11. 删除文件                      rm -rf + <filename/path>




    