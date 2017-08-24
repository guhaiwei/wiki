### Git 常用命令查询表
安装gitlab步骤<https://about.gitlab.com/installation/>
#### 创建版本库   
`git clone https://github.com/guhaiwei/wiki`#克隆远程版本库<br/>
`git init`#初始化本地版本库<br/>

#### 修改和提交   
`git status` #查看状态<br/>
`git diff` #查看变更内容<br/>
`git add .` #跟踪所有改动过的文件<br/>
`git add <file>` #跟踪置顶文件<br/>
`git mv <old> <new>` #文件改名<br/>
`git rm <file>` #删除文件<br/>
`git rm -cached <file>` #停止跟踪文件单不删除<br/>
`git commit -m "commit message"` #提交所有更新过的文件<br/>
`git commit -amend` #修改最后一次提交<br/>

#### 查看提交历史
`git log` #查看提交历史<br/>
`git log -p <file>` #查看置顶文件的提交历史<br/>
`git blame <file>` #以列表的方式查看置顶文件的提交历史<br/>

#### 撤消
`git reset --hard HEAD` #撤消工作目录中所有未提交的文件的修改内容<br/>
`git checkout HEAD <file>` #撤消置顶的为条件文件的修改内容<br/>
`git revert <commit>` #撤消置顶的提交<br/>

#### 分支与标签
`git branch` #显示所有以本地分支<br/>
`git checkout <branch/tag>` #切换到置顶分支或标签<br/>
`git branch <new-branch>` #创建新分支<br/>
`git branch -d <branch>` #删除本地分支<br/>
`git tag` #列出所有本地tag<br/>
`git tag <tagname>` #基于最新提交创建tag<br/>
`git tag -d <tagname>` #删除tag<br/>

#### 合并与衍合
`git merge <branch>` #合并置顶分支到当前分支<br/>
`git rebase <branch>` #衍合之定义分支到当前分支<br/>

#### 远程操作
`git remote -v` #查看远程版本库信息<br/>
`git remote show <remote>` #查看置顶远程版本库信息<br/>
`git remote add <remote> <url>` #添加远程版本库<br/>
`git fetch <remote>` #从远程版本库获取代码（不自动合并）<br/>
`git pull <remote> <branch>` #下载代码级快速合并<br/>
`git push <remote> <branch>` #上传代码并快速合并<br/>
`git push <remote> ;<branch/tag-name>` #删除远程分支或tag<br/>
`git push --tags` #上传所有tag<br/>


