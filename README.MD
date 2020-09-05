##1,git config --global user.name ""
 	git config --global user.email "" 
	git config --list 
	
2 git status命令
	git add test.txt 添加文件
	git rm --cached test.txt 删除暂存区文件
	git commit -m 'first commit' 
	git log 查看提交历史

3 查看修改 git diff 
4 删除文件
    在本地删除文件
    git add 被删除的文件民
    git commit -m 'message'
5 重命名文件
    git mv 文件1 文件2 将文件1重命名为文件2
6 移动文件到文件夹
    git mv 文件 路径/可选名字 例如: git mv about.txt file/