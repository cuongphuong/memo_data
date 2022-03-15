---
id: 1647358835249
title: Just-In-Time Compiler
category: Java Language/Core/
---

Trong khi trình biên dịch bình thường chịu trách nhiệm biên dịch tất cả mã khi chúng ta chạy chương trình, chuyển đổi mã sang nhị phân và tạo tệp thực thi, trình biên dịch JIT tối ưu hóa công việc này bằng cách chỉ biên dịch mã của từng chức năng khi cần thiết. .

Theo cách này, khi chúng ta thực thi một chương trình, trình biên dịch Just-In-Time, hoặc JIT, sẽ chỉ biên dịch các hàm sẽ được sử dụng tại thời điểm đó, lưu kết quả vào bộ nhớ cache. Khi chúng ta sử dụng chương trình, khi chúng ta gặp một hàm mới chưa được biên dịch, nó sẽ được biên dịch lại. Tuy nhiên, khi chúng tôi tìm thấy một chức năng đã được sử dụng, thay vì biên dịch lại, nó sẽ được tìm kiếm trong bộ nhớ đệm, giúp tiết kiệm một lượng thời gian đáng kể.

**VD:** `OpenJ9 `(Trình biên dịch Eclipse JIT cho mã Java )

![Compilar-JIT-Java.webp](https://raw.githubusercontent.com/cuongphuong/memo_data/main/Images/1647358783138_Compilar-JIT-Java.webp)