## 初始化工作区
`git init`

## 全局配置
`git config --global user.name 'xxxx'`
`git config --global user.email 'xxxxx@xx.com'`

## 查看状态
`git status`

## 将工作区指定的内容添加到暂存区
`git add 文件夹或文件`

## 将暂存区的内容提交到本地仓库，生成版本
`git commit -m '备注信息'`

## 查看提交详细日志(不包括被丢弃的版本)
`git log`

## 查看提交精简日志(不包括被丢弃的版本)
`git log --oneline`

## 查看所有操作日志，包括被丢弃的版本
`git reflog`

## 仅重置本地仓库
`git reset --soft 版本号`

## 重置本地仓库和暂存区(--mixed 为默认值)
`git reset 版本号` 或 `git reset --mixed 版本号`

## 重置本地仓库、暂存区和工作区(比较危险，会覆盖正在开发的代码)
`git reset --hard 版本号`

## 忽略相关
创建 .gitignore 文件，在该文件里添加要忽略的文件
。gitignore 文件用 # 表示注释
```gitignore
# 指定 git 忽略的文件
test.html

# 忽略所有文件名是 test 的文件，不管后缀是什么
test.*

# 忽略所有后缀是 .tmp 的文件，不管文件名是什么
*.tmp

# 取反，不忽略 test.tmp 文件，让 git 管理
!test.tmp

# 忽略 node_modules 目录下的所有文件
node_modules/

# git 管理的是文件，如果目录为空，git 会自动忽略该目录
```

## 分支工作流
```text
只在 master 分支上保留完全稳定的分支
在 dev 分支上做开发，最终合并到 master 分支上
在 hotfix 分支上进行紧急修复，最终合并到 master 分支上
还可以有更多分支(分支名可以随意起)
```

## 查看分支
`git branch` 或 `git branch -v`
`git branch -v` 查看的信息比较详细，会有提交时的备注信息

## 在当前分支的节点上创建新的分支
`git branch 分支名`

## 切换分支
`git checkout 分支名` 或 `git switch 分支名`
`git switch 分支名` 是 git v2.23.0 以后的版本才支持，所以会有兼容性问题

## 合并分支
先切换到要合并的分支上
`git checkout master`
将 hotfix 合并到 master 上
`git merge hotfix`

## 删除分支
`git branch -d hotfix`
