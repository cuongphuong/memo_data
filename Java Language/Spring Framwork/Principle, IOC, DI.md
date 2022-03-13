---
id: 1647139464817
title: Principle, IOC, DI
category: Java Language/Spring Framwork/
---

Sự khác biệt giữa 3 khái niệm trên:

* **`Dependency Inversion:`** Đây là một nguyên lý để thiết kế và viết code.

* **`Inversion of Control:`** Đây là một design pattern được tạo ra để code có thể tuân thủ nguyên lý Dependency Inversion. Có nhiều cách hiện thực pattern này: `ServiceLocator`, `Event`, `Delegate`, … `Dependency Injection` là một trong các cách đó.

* **`Dependency Injection:`** Đây là một cách để hiện thực Inversion of Control Pattern (Có thể coi nó là một design pattern riêng cũng được). Các module phụ thuộc (dependency) sẽ được inject vào module cấp cao.

![ioc-and-mapper-in-c-6-638.webp](https://raw.githubusercontent.com/cuongphuong/memo_data/main/Images/1647139444793_ioc-and-mapper-in-c-6-638.webp)


Source: [https://toidicodedao.com/2015/11/03/dependency-injection-va-inversion-of-control-phan-1-dinh-nghia/]()