---
id: 1647069687507
title: Stack và Heap
category: Java Language/Wiki/
---

|Đặc điểm|Stack|Heap|
| --- | --- | --- |
|Memory|Bộ nhớ stack chỉ được sử dụng bởi một luồng thực thi|Bộ nhớ Heap được sử dụng bởi tất cả các phần của ứng dụng|
|Access|các luồng khác không thể truy cập vào bộ nhớ stack|các đối tượng được lưu trữ trong heap có thể được truy cập ở mọi nơi|
|Memory Management|Sử dụng LIFO để giải phóng bộ nhớ|Phải giải phóng thông qua lập trình viên|
|Lifetime|Tồn tại cho đến khi kết thúc quá trình thực thi luồng|Tồn tại từ khi bắt đầu cho đến khi kết thúc quá trình thực thi ứng dụng|
|Usage|Stack chỉ chứa các biến local primitive và tham chiếu đến các đối tượng trong heap space|Bất cứ khi nào đối tượng được tạo, nó luôn được lưu trữ trong heap space|