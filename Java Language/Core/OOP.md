---
id: 1647360345518
title: OOP
category: Java Language/Core/
---

**`OOP`** bao gồm:
* Kế thừa (Inheritance)
* Đóng gói (Encapsulation)
* Đa hình (Polymorphism)
* Trừu tượng (Abtraction)

---

##### Kế thừa (Inheritance)
Kế thừa có nghĩa là một lớp có thể mở rộng sang lớp khác. Vì vậy, các mã có thể được sử dụng lại từ lớp này sang lớp khác. Lớp hiện có được gọi là lớp cha trong khi lớp dẫn xuất được gọi là lớp con.

---
##### Đóng gói ( Encapsulation)
Bảo vệ code từ bên ngoài.

Bảo trì code.

Trong Java, tính đóng gói được thể hiện thông qua phạm vi truy cập (`access modifier`). Ngoài ra, các lớp liên quan đến nhau có thể được gom chung lại thành `package`.

---
##### Đa hình (Polymorphism) 

Tính đa hình là khả năng một đối tượng có thể thực hiện một tác vụ theo nhiều cách khác nhau.

Trong Java, chúng ta sử dụng nạp chồng phương thức (method overloading) và ghi đè phương thức (method overriding) để có tính đa hình.

`Nạp chồng (Overloading)`: Đây là khả năng cho phép một lớp có nhiều thuộc tính, phương thức cùng tên nhưng với các tham số khác nhau về loại cũng như về số lượng. 

`Ghi đè (Overriding)`: là hai phương thức cùng tên, cùng tham số, cùng kiểu trả về nhưng thằng con viết lại và dùng theo cách của nó, và xuất hiện ở lớp cha và tiếp tục xuất hiện ở lớp con. 

---

##### Tính trừu tượng (abstraction)
Tính trừu tượng là một tiến trình ẩn các chi tiết trình triển khai và chỉ hiển thị tính năng tới người dùng. Tính trừu tượng cho phép bạn loại bỏ tính chất phức tạp của đối tượng bằng cách chỉ đưa ra các thuộc tính và phương thức cần thiết của đối tượng trong lập trình.

Tính trừu tượng giúp bạn tập trung vào những cốt lõi cần thiết của đối tượng thay vì quan tâm đến cách nó thực hiện.

Trong Java, chúng là sử dụng `abstract class` và `abstract interface` để có tính trừu tượng.
