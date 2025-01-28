# Git

删除 Git 仓库中的所有提交记录，但保留当前代码状态

```sh
# 1. 创建一个新的孤立分支（没有提交历史）
git checkout --orphan new_branch

# 2. 添加所有文件到暂存区
git add -A

# 3. 提交更改
git commit -m "Initial commit"

# 4. 删除旧分支
git branch -D main

# 5. 重命名新分支
git branch -m main

# 6. 强制推送更改到远程仓库
git push --force origin main
```
