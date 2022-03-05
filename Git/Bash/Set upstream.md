---
id: 1646460402191
title: Set upstream
category: Git/Bash/
---

Để sử dụng lệnh (VD: `git pull`, `git push -f`) mà không cần chỉ định remote name (`origin`) thì cần set upstream cho branch bằng cách nhập lệnh sau:
```
git branch --set-upstream-to=origin/<branch> branchName
```
