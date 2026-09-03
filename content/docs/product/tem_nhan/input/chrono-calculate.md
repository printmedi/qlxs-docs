---
bookFlatSection: true
weight: 50
type: docs
title: Tính Toán Thời Gian
url: /tem_nhan/chrono-calculate
---

# Kết Quả Tính Toán Thời Gian Cho In Tem nhãn

Dưới đây là những kết quả tính toán liên quan tới giá trị thời gian cho đơn in Tem nhãn.

## Thời gian chế bản
**Thời gian tiền kỳ thuộc phạm vi model**

- **Tổng thời gian chế bản thuộc model**
  * *V1 chưa định lượng workflow artwork/RIP/làm bản riêng; trả 0 minh bạch thay vì dùng công thức Sách.*
  * *Đơn vị*: Phút
  * *Mã*: TCCTPREPRESS
  * *Kí hiệu*: {{< katex >}}T_{pre}{{< /katex >}}

## Thời gian in và bế inline
**Thời gian chiếm dụng máy flexo cuộn tích hợp**

- **In flexo và bế inline**
  * *Một stage tích hợp theo tổng mét web; không cộng bế inline lần hai.*
  * *Đơn vị*: Phút
  * *Mã*: TCCPRINT
  * *Kí hiệu*: {{< katex >}}T_p{{< /katex >}}

- **Tổng thời gian in**
  * *Tổng thời gian chiếm dụng máy in cuộn trong model.*
  * *Đơn vị*: Phút
  * *Mã*: TCCTPRINT
  * *Kí hiệu*: {{< katex >}}T_{print}{{< /katex >}}

## Thời gian hoàn thiện
**Thời gian chia cuộn offline**

- **Chia cuộn tem**
  * *Thời gian máy chia/kiểm tra/rewind offline theo tổng mét web.*
  * *Đơn vị*: Phút
  * *Mã*: TCCSLIT
  * *Kí hiệu*: {{< katex >}}T_s{{< /katex >}}

- **Tổng thời gian hoàn thiện**
  * *Tổng stage hoàn thiện được processing bật.*
  * *Đơn vị*: Phút
  * *Mã*: TCCTCOMP
  * *Kí hiệu*: {{< katex >}}T_{finish}{{< /katex >}}



