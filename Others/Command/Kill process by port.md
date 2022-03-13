---
id: 1647152418829
title: Kill process by port
category: Others/Command/
---


**1. For Windows**


```
netstat -ano | findstr :yourPortNumber
```


---
![ue3dJ.png](https://raw.githubusercontent.com/cuongphuong/memo_data/main/Images/1647151507769_ue3dJ.png)



```
taskkill /pid yourid /f
```


---

![G2gKF.png](https://raw.githubusercontent.com/cuongphuong/memo_data/main/Images/1647151525109_G2gKF.png)


**1. For Linux/Mac**

```
sudo kill -9 $(sudo lsof -t -i:8080)
```
