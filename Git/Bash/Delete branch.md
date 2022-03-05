---
id: 1646460296850
title: Delete branch
category: Git/Bash/
---

Checkout sang branch khác, nhập lệnh sau để xóa branch trên local repository:
```
// delete branch locally
git branch -d localBranchName
```

Nếu branch có tồn tại trên remote repository, để xóa thì nhập lệnh sau:
```
// delete branch remotely
git push origin --delete remoteBranchName
```
