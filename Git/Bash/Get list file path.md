---
id: 1646460485147
title: Get list file path
category: Git/Bash/
---

Get danh sách file thay đổi so với master và xuất danh sách ra file thì nhập lệnh sau
(Có thể bỏ ` >filePath.txt` để xuất trực tiếp ra console log `git bash`

```
git diff --name-only master >filePath.txt
```
