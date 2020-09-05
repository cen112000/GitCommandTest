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
        7 快速提交
            git commit -am 'dfsdf' 相当于 git add . git commit -m ''
        8 恢复被删除的文件 
            git checkout -- file 不能操作暂存区里的文件
            git reset HEAD file 不在追踪暂存区文件 然后再使用git checkout -- file 恢复内容
        9 版本回退
            git reset --hard 哈希值 回退到指定版本，但该版本之后的所有操作将不再保留
        10 回退到旧版本 git log 拿到版本号hash，git checkout hash -- file , git commit -m '' 

        git连接远程仓库 git remote add gm(任意名) 远程仓库地址
        git push -u gm master 推送到远程仓库master分支

        查看分支 git branch 。git branch -a ,git branch -r 。
        切换分支 git checkout 分支名 。
        创建分支 git branch 分支名。
        快速创建，切换分支 git checkout -b 分支名。
        删除分支 git branch -d（/D强制删除） 分支名。
        删除分支再恢复原来的分支 git branck 原来分支民 hash值（删除分支时的hash值）
        分支合并 git merge 
        合并冲突，解决后，git add . ,git commit 不带-m。

        添加版本线图 git log --oneline --graph
        不添加快转合并 git merge 分支名 --no-ff
        git merge 分支名 --no-ff --no-commit 不提交合并
        恢复到合并之前 git reset --hard ORIG_HARD
        
        删除已经合并的分支
            git branch --merged | egrep -v "(^\*|master|dev)" | xargs git branch -D
        删除未合并的分支
            git branch --no-merged | egrep -v "(^\*|master|dev)" | xargs git branch -D


