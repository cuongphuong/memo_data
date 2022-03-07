---
id: 1646635955341
title: Rename branch Git
category: Git/Bash/
---

Rename branch

1. Đổi tên
```
git branch -m new-name
git push origin :old-name new-name
```
2. Set lại `upstream` hoặc update remote origin tại `.git/config`