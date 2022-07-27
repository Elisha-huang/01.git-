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
