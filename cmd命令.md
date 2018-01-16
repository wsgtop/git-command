# CMD命令

## 磁盘管理

<table>
	<tr>
		<th> diskpart </th>
		<th> 进入磁盘管理 </th>
	</tr>

	<tr>
		<th> select + 磁盘代号  </th>
		<th> 进入相应磁盘 </th>
	</tr>
	<tr>
		<th> clean  </th>
		<th> 清除当前物理磁盘全部数据 </th>
	</tr>
	<tr>
		<th> detail disk   </th>
		<th> 查看磁盘的详细信息 </th>
	</tr>
	<tr>
		<th> list disk   </th>
		<th> 查询磁盘，显示磁盘数量和磁盘代号（列出电|脑上所有的物理磁盘） </th>
	</tr>
</table>	

## 创建文件

	echo  显示一段文字，一般起到一个提示的作用,例如echo string ,会在页面打印string
	
	echo nul>*.*  将一个内容为空的放入到*.*的文件中，如果这个文件不存在，就创建一个
	
	echo nul>.txt 创建一个txt类型的文件，该文件没有文件名，文件内容为空
	
	echo nul>123.txt  创建一个文件名为123的txt类型的文件，文件内容为空
	
	echo 1243>123.txt 创建一个文件名为123的txt类型的文件，文件内容为1243，如果123.txt文件存在且有内容，则先清空内容再添加内容1243
	
	echo 1243>>123.txt 创建一个文件名为123的txt类型的文件，文件内容为1243，如果123.txt文件存在且有内容，则再末尾换行追加内容1243

