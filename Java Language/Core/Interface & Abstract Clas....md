---
id: 1647360650416
title: Interface & Abstract Class
category: Java Language/Core/
---


#### Interface 

Không thể đa kế thừa trong java. Để khắc phục vấn đề này Khái niệm interface được giới thiệu.

Interface là một mẫu chỉ có khai báo phương thức và không thực hiện phương thức (hành vi).

---

* Tất cả các phương thức trong interface là public abstract void. .
* Tất cả các biến trong interface là public static final.
* Các lớp có thể implement interface và không extends.
* Lớp implement interface sẽ cung cấp một triển khai cho tất cả các phương thức được khai báo trong interface.


#### Abstract Class
Có thể tạo lớp Trừu tượng bằng cách sử dụng từ khóa "Abstract"  trước tên lớp. Một lớp trừu tượng có thể có cả các phương thức Abstract và các phương thức Non-Abstract .

